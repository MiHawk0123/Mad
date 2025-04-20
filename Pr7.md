#7
XML (activity_main.xml):

------------------------

<LinearLayout 

 xmlns:android="http://schemas.android.com/apk/res/android"

 android:orientation="vertical"

 android:layout_width="match_parent"

 android:layout_height="match_parent"

 android:gravity="center"

 android:padding="16dp">

 <ProgressBar android:id="@+id/progressBar"

 style="?android:attr/progressBarStyleHorizontal"

 android:layout_width="match_parent"

 android:layout_height="wrap_content"

 android:progress="50"

 android:max="100"/>

</LinearLayout>

Java (MainActivity.java):

-------------------------

package com.example.progressbar;

import android.os.Bundle;

import android.widget.ProgressBar;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

 ProgressBar progressBar;

 @Override

 protected void onCreate(Bundle savedInstanceState) {

 super.onCreate(savedInstanceState);

 setContentView(R.layout.activity_main);

 progressBar = findViewById(R.id.progressBar);

 progressBar.setProgress(70); // Example

 }

}
