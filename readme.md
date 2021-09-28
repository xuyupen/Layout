#                 实验二 Android界面布局

##     一，线性布局

​    

- 创建新的布局文件使用线性布局

- 一个垂直的线性布局里嵌套4个水平线性布局

- 新建drawable文件，将设置边框格式的代码写入

- Text view引用drawable文件

- 关键代码：第一行的实现代码

    

  ```xml
  <LinearLayout
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:orientation="horizontal"
      >
      <TextView
          android:layout_width="0dp"
          android:layout_height="wrap_content"
          android:layout_weight="1"
          android:background="@drawable/underline"
          android:hint="@string/OneOne" />
  
      <TextView
          android:layout_width="0dp"
          android:layout_height="wrap_content"
          android:layout_weight="1"
          android:background="@drawable/underline"
          android:hint="@string/OneTwo" />
  
      <TextView
          android:layout_width="0dp"
          android:layout_height="wrap_content"
          android:layout_weight="1"
          android:background="@drawable/underline"
          android:hint="@string/OneThree" />
  
      <TextView
          android:layout_width="0dp"
          android:layout_height="wrap_content"
          android:layout_weight="1"
          android:background="@drawable/underline"
          android:hint="@string/OneFour" />
  </LinearLayout>
  ```

- 实现效果：

![](https://github.com/xuyupen/test2/blob/7573a657b1c2c80dc23fd7f24d1c5622a18127c4/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202021-09-28%20121338.png)

##    二，约束布局

- 创建布局文件，默认为约束布局

- 使用Design

- 拖动左上方工具新建两个Text view，内容为input ，0.0。右侧工具栏设置相关属性。设置约束

- 新建4个Text view，一行设置相同的垂直约束，相邻两个Text view 依次建立约束。

- 剩下的三行设置方法同第一行。

- 关键代码：设置第一行的代码

  ```xml
   <TextView
          android:id="@+id/textView14"
          android:layout_width="60dp"
          android:layout_height="40dp"
          android:layout_marginTop="20dp"
          android:text="@string/seven"
          android:gravity="center"
          app:layout_constraintBottom_toBottomOf="parent"
          app:layout_constraintEnd_toEndOf="parent"
          app:layout_constraintHorizontal_bias="0.0"
          app:layout_constraintStart_toStartOf="@+id/textView3"
          app:layout_constraintTop_toBottomOf="@+id/textView3"
          app:layout_constraintVertical_bias="0.0" />
  
      <TextView
          android:id="@+id/textView15"
          android:layout_width="60dp"
          android:layout_height="40dp"
          android:gravity="center"
          android:layout_marginStart="20dp"
          android:layout_marginTop="20dp"
          android:text="@string/eight"
          app:layout_constraintBottom_toBottomOf="parent"
          app:layout_constraintEnd_toEndOf="parent"
          app:layout_constraintHorizontal_bias="0.015"
          app:layout_constraintStart_toEndOf="@+id/textView17"
          app:layout_constraintTop_toBottomOf="@+id/textView3"
          app:layout_constraintVertical_bias="0.0" />
  
      <TextView
          android:id="@+id/textView16"
          android:layout_width="60dp"
          android:layout_height="40dp"
          android:gravity="center"
          android:layout_marginStart="20dp"
          android:layout_marginTop="20dp"
          android:text="@string/nine"
          app:layout_constraintBottom_toBottomOf="parent"
          app:layout_constraintEnd_toEndOf="parent"
          app:layout_constraintHorizontal_bias="0.0"
          app:layout_constraintStart_toEndOf="@+id/textView14"
          app:layout_constraintTop_toBottomOf="@+id/textView3"
          app:layout_constraintVertical_bias="0.0" />
  
      <TextView
          android:id="@+id/textView17"
          android:layout_width="60dp"
          android:layout_height="40dp"
          android:layout_marginStart="20dp"
          android:layout_marginTop="20dp"
          android:text="@string/chu"
          android:gravity="center"
          app:layout_constraintBottom_toBottomOf="parent"
          app:layout_constraintEnd_toEndOf="parent"
          app:layout_constraintHorizontal_bias="0.006"
          app:layout_constraintStart_toEndOf="@+id/textView16"
          app:layout_constraintTop_toBottomOf="@+id/textView3"
          app:layout_constraintVertical_bias="0.0" />
  ```

-    实现效果:

  ![](https://github.com/xuyupen/test2/blob/588211ba38b1066428836284431ef49ae7f78b3f/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202021-09-28%20123348.png)

##    三，表格布局    

- 创建表格布局

- 令其属性 android：stretchColumns="1"  

- 一个<TableRow>里    创建相应个数的Text view

- 第四，七行设置为分割线

- 关键代码：第一行代码和第四行分割线

  ```xml
  <TableRow>
  
      <TextView
          android:layout_width="208dp"
          android:layout_height="30dp"
          android:text="@string/open"
          android:textSize="20sp"
          />
      <TextView
          android:layout_height="30dp"
          android:gravity="right"
          android:text="@string/CtrlO"
          android:textSize="20sp"
        />
  </TableRow>
  ```

​    

```xml
<TableRow android:background="#EC407A">
    <TextView android:layout_height="3dp" />
</TableRow>
```

- 实现效果：

  ![](https://github.com/xuyupen/test2/blob/86e64183dab0f2337076ff21af0dbe1ea86aecec/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202021-09-28%20123313.png)

