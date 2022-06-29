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
implementation 'com.github.vocsyurvish:Recycler-Utils:1.0.0'
```

# Features and classes to use.

## ● SnapHelperOneByOne
- **SnapHelperOneByOne** use for scroll each items one by one.
- How to use.

```java
//create object of SnapHelper
SnapHelper snapHelper = new SnapHelperOneByOne()
//attach to recyclerview...
snapHelper.attachToRecyclerView(YOUR_RECYCLER_VIEW);
```

## ● CenterZoomLayoutManager
- **CenterZoomLayoutManager** use for zoom center item of recyclerview.
- How To Use

```java
//create object
CenterZoomLayoutManager manager = new CenterZoomLayoutManager(this, RecyclerView.HORIZONTAL, false);
//attach to recyclerview
YOUR_RECYCLER_VIEW.setLayoutManager(manager);
//notify manager
YOUR_RECYCLER_VIEW.smoothScrollBy(1, 1);
```

## ●  EndlessRecyclerViewScrollListener
- **EndlessRecyclerViewScrollListener** use for pagination
- How to use

```java
 YOUR_RECYCLER_VIEW.addOnScrollListener(new EndlessRecyclerViewScrollListener(YOUR_LAYOUT_MANAGER) {
            @Override
            public void onLoadMore(int page, int totalItemsCount) {
             	//write your logic here...
            }
        });
```
