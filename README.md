
# Rapport
Jag skapade även ett fragment i vilken jag la till en bild och en text.
```
    <ImageView
        android:id="@+id/imageView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_weight="1"
        android:src="@android:drawable/ic_delete"
        android:layout_gravity="center_horizontal"
        android:layout_marginBottom="10dp"/>
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/hello_blank_fragment" />

```

Skapade sedan en ny vy i vilken jag la till den fragmentet.
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center"
    tools:context=".MainActivity">
    <LinearLayout
        android:orientation="vertical"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="center">

        <fragment
            android:id="@+id/fragment"
            android:name="com.example.screens.BlankFragment"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" />
    </LinearLayout>
</LinearLayout>
```

Till sist länkade jag första vyn till andra vyn med en knapp i första vyn.

```
    public void openSecondaryActivity(View view) {
        Intent intent = new Intent(this, SecondaryActivity.class);
        startActivity(intent);
```

```
        <Button
            android:id="@+id/button"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:onClick="openSecondaryActivity"
            android:text="DO NOT PUSH!" />
```
