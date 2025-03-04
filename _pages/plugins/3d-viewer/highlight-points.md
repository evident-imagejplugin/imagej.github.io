---
mediawiki: 3D_Viewer:_Highlight_Points
title: 3D Viewer › Highlight Points
nav-links: true
nav-title: Highlight Points
---

## How to highlight named points of a Content

You can download example source code for this HowTo [here](/plugins/3d-viewer/example-code).

Each `Content` owns a list of named points, which may e.g. be used to mark specific positions. By default, the point list is not shown, but it can be switched on, which displays the points as spheres in the universe and opens a dialog showing a list of the points.

The following example shows how to retrieve the point list of a `Content` and add a few points:

```java
// Add the image as a volume
Content c = univ.addVoltex(imp);


// Make the point list visible
c.showPointList(true);

// Retrieve the point list
PointList pl = c.getPointList();

// Add a few points
pl.add(190, 450, 170);

pl.add(330, 370, 300);

pl.add(430, 90, 150);
```

The coordinates specified to create a new point are local coordinates of the corresponding `Content`.

Sometimes, it's convenient to select a point on the surface of a `Content` at a specific canvas position. This is also possible, by using the `Picker` class. A reference to a `Picker` object can be obtained from the universe:

```java
// Add a point at a specific canvas position
univ.getPicker().addPoint(c, 256, 256);
```
The points have a default size, which can be changed:

```java
// Change the size of the points
float curr = c.getLandmarkPointSize();
c.setLandmarkPointSize(curr * 2);
```

To delete the first point in the list;

```java
// delete the first point
pl.remove(0);
```

To rename a point:

```java
// rename the now first point
pl.rename(pl.get(0), "newName");
```
To change the position of a point:

```java
// change the position of the now first point
pl.placePoint(pl.get(0), 190, 450, 170);
```

### Important methods regarding landmark points

Important methods are found in `Content.java` and `PointList.java`.

<b>`Content.java:`</b>

        public void showPointList(boolean b);

        public PointList getPointList();

        public void loadPointList();

        public void savePointList();

        public float getLandmarkPointSize();

        public void setLandmarkPointSize(float r);

<b>`PointList.java`:</b>

        public void add(BenesNamedPoint point);

        public void add(String name, double x, double y, double z);

        public void add(double x, double y, double z);

        public void remove(BenesNamedPoint point);

        public void remove(int i);

        public void clear();

        public void rename(BenesNamedPoint point, String name);

        public void up(BenesNamedPoint point);

        public void down(BenesNamedPoint point);

        public void highlight(BenesNamedPoint p);

        public void placePoint(BenesNamedPoint point,
                    double x, double y, double z);

        public BenesNamedPoint get(int index);

        public int indexOf(BenesNamedPoint p);

        public int indexOfPointAt(double x, double y, double z, double tol);

        public BenesNamedPoint pointAt(double x, double y, double z, double tol);

        public int size();

        public BenesNamedPoint get(String name);

        public Iterator iterator();

Both `Content.java` and `PointList.java` provide a `save()` and `load()` method, but it is highly recommended to use that of `Content.java`.
