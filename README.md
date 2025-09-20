dview-flash-view
![Release](https://jitpack.io/v/dora4/dview-flash-view.svg)
--------------------------------

#### 运行效果
![高亮炫光](https://github.com/user-attachments/assets/31a7733d-444d-44fd-84b4-d420238107c6)

#### 卡片
![DORA视图 激光生成器](https://github.com/user-attachments/assets/e1c61a9c-57cf-4b38-b0fc-46df9c55f228)

#### 规范标准
此控件遵循《Dora View规范手册》 https://github.com/dora4/dview-template/blob/main/Naming_Convention_Guide.md

#### Gradle依赖配置

```groovy
// 添加以下代码到项目根目录下的build.gradle
allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}
// 添加以下代码到app模块的build.gradle
dependencies {
    implementation 'com.github.dora4:dview-flash-view:1.1'
}
```

#### 使用方式
activity_flash_view.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<layout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    tools:context=".ui.FlashViewActivity">

    <data>

    </data>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical">

        <dora.widget.DoraTitleBar
            android:id="@+id/titleBar"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:background="@color/colorPrimary"
            app:dview_title="@string/common_title" />

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:orientation="vertical"
            android:gravity="center_horizontal"
            android:padding="5dp">

            <dora.widget.DoraFlashView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_margin="10dp"
                android:padding="10dp"
                app:dview_fv_rotateAngle="30">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="20dp"
                    android:gravity="center"
                    android:text="顺时针倾斜"
                    android:textColor="@color/white"
                    android:textStyle="bold" />
            </dora.widget.DoraFlashView>

            <dora.widget.DoraFlashView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_margin="10dp"
                android:padding="10dp"
                app:dview_fv_bgColor="@color/girl_pink"
                app:dview_fv_rotateAngle="0">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="20dp"
                    android:gravity="center"
                    android:text="垂直"
                    android:textColor="@color/white"
                    android:textStyle="bold" />
            </dora.widget.DoraFlashView>

            <dora.widget.DoraFlashView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_margin="10dp"
                android:padding="10dp"
                app:dview_fv_bgColor="@color/gold_yellow"
                app:dview_fv_rotateAngle="-30">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="20dp"
                    android:gravity="center"
                    android:text="逆时针倾斜"
                    android:textColor="@color/white"
                    android:textStyle="bold" />
            </dora.widget.DoraFlashView>

            <dora.widget.DoraFlashView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_margin="10dp"
                android:padding="10dp"
                app:dview_fv_bgColor="@color/vibrant_orange"
                app:dview_fv_deltaX="50dp"
                app:dview_fv_rotateAngle="30">

                <TextView
                    android:layout_width="match_parent"
                    android:layout_height="20dp"
                    android:gravity="center"
                    android:text="加速"
                    android:textColor="@color/white"
                    android:textStyle="bold" />
            </dora.widget.DoraFlashView>

            <dora.widget.DoraFlashView
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="10dp"
                app:dview_fv_gradientSize="100dp"
                app:dview_fv_highlightColor="#7fffff00"
                app:dview_fv_rotateAngle="30"
                app:dview_fv_type="blur">

                <ImageView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:layout_gravity="center_horizontal"
                    android:src="@drawable/by_jose_royo" />
            </dora.widget.DoraFlashView>

            <dora.widget.DoraFlashView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_margin="10dp"
                android:padding="10dp"
                app:dview_fv_deltaX="15dp"
                app:dview_fv_gradientSize="200dp"
                app:dview_fv_rotateAngle="45"
                app:dview_fv_type="blur">
                <!-- 留出内边距相框效果 -->
                <ImageView
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:layout_gravity="center_horizontal"
                    android:background="@drawable/by_tom_toles" />
            </dora.widget.DoraFlashView>
        </LinearLayout>
    </LinearLayout>

</layout>
```
