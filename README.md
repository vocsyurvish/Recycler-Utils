# RecyclerView Utility  [![Release](https://jitpack.io/v/vocsyurvish/Recycler-Utils.svg)](https://jitpack.io/#vocsyurvish/Recycler-Utils) [![API](https://img.shields.io/badge/API-21%2B-yellow.svg?style=flat)](https://android-arsenal.com/api?level=21)
### import library in your project...

```groovy
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```
- add into dependencies.
```groovy
implementation 'com.github.vocsyurvish:Recycler-Utils:LATEST_VERSION'
```

### ● SmoothScrollness
###### **SmoothScrollness** use for smooth scroll on recyclerview.

```java
SnapHelper snapHelper = new SmoothScrollness(HOW_MUCH_SMOOTH /*int*/);
snapHelper.attachToRecyclerView(YOUR_RECYCLER_VIEW);
```

### ● SnapHelperOneByOne
###### **SnapHelperOneByOne** use for scroll each items one by one.

```java
//create object of SnapHelper
SnapHelper snapHelper = new SnapHelperOneByOne()
//attach to recyclerview...
snapHelper.attachToRecyclerView(YOUR_RECYCLER_VIEW);
```

### ● CenterZoomLayoutManager
###### **CenterZoomLayoutManager** use for zoom center item of recyclerview.

```java
//create object
CenterZoomLayoutManager manager = new CenterZoomLayoutManager(this, RecyclerView.HORIZONTAL, false);
//attach to recyclerview
YOUR_RECYCLER_VIEW.setLayoutManager(manager);
//notify manager
YOUR_RECYCLER_VIEW.smoothScrollBy(1, 1);
```

### ●  EndlessRecyclerViewScrollListener
###### **EndlessRecyclerViewScrollListener** use for pagination

```java
 YOUR_RECYCLER_VIEW.addOnScrollListener(new EndlessRecyclerViewScrollListener(YOUR_LAYOUT_MANAGER) {
            @Override
            public void onLoadMore(int page, int totalItemsCount) {
             	//write your logic here...
            }
        });
```

### ●  OverNestedScrollView
###### **OverNestedScrollView** use for Over scroll effect in recyclerView
###### xml Side

```xml
<com.urvish.utility.recycler_utils.OverNestedScrollView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:fillViewport="true"
        android:overScrollMode="ifContentScrolls"
        android:scrollbarStyle="outsideOverlay"
        android:scrollbars="vertical">
	
	<!-- YOUR_RECYCLERVIEW -->l̥
	
</com.urvish.utility.recycler_utils.OverNestedScrollView>
```

###### Java Side
```java
YOUR_RECYCLERVIEW.setNestedScrollingEnabled(false);
```
