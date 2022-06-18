# TouchStudy
 滑动冲突学习

## 需求
能在 ScrollView 下长按移动绘制矩形，并且如果长按移动到了屏幕边缘可以使 ScrollView 滚动  

由于移动到边缘再滚动与滑动冲突的关系不是很大，所以就未实现，但注释中提供了思路

## 用到的方法
- 外部拦截法
- 内部拦截法
- 重写 dispatchTouchEvent 法

## 注意事项
如果你在快速滑动 ScrollView 后立马再次触摸，此时是不能激活长按的，原因在于 ScrollView 会在 Down 事件时
判断自己是否处于上一次滑动后的惯性滑动，如果处于的话，就默认直接拦截事件。