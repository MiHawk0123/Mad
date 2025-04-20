#6( Linear Layout with Name, Age, Mobile)
XML (activity_main.xml):

------------------------

<LinearLayout 

 xmlns:android="http://schemas.android.com/apk/res/android"

 android:orientation="vertical"

 android:layout_width="match_parent"

 android:layout_height="match_parent"

 android:padding="16dp">

 <EditText android:layout_width="match_parent"

 android:layout_height="wrap_content" android:hint="Name" />

 <EditText android:layout_width="match_parent"
 android:layout_height="wrap_content" android:hint="Age" android:inputType="number" />

 <EditText android:layout_width="match_parent"

 android:layout_height="wrap_content" android:hint="Mobile Number" android:inputType="phone" />

</LinearLayout>
