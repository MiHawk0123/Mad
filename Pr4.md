#pr 4
XML (activity_main.xml):

------------------------

<LinearLayout 

 xmlns:android="http://schemas.android.com/apk/res/android"

 android:orientation="vertical"

 android:layout_width="match_parent"

 android:layout_height="match_parent"

 android:padding="16dp"

 android:gravity="center">

 <AutoCompleteTextView android:id="@+id/autoSearch" android:layout_width="match_parent"

 android:layout_height="wrap_content" android:hint="Search here" />

</LinearLayout>

Java (MainActivity.java):

-------------------------

package com.example.searchengine;

import android.os.Bundle;

import android.widget.ArrayAdapter;

import android.widget.AutoCompleteTextView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

 AutoCompleteTextView autoSearch;

 String[] searchItems = {"Google", "Yahoo", "Bing", "DuckDuckGo", "Ask"};

 @Override

 protected void onCreate(Bundle savedInstanceState) {

 super.onCreate(savedInstanceState);

 setContentView(R.layout.activity_main);

 autoSearch = findViewById(R.id.autoSearch);

 ArrayAdapter<String> adapter = new ArrayAdapter<>(this,

 android.R.layout.simple_list_item_1, searchItems);

 autoSearch.setAdapter(adapter);

 }

}
