#pr 5 
MainActivity.java

import android.os.Bundle;

import android.view.View;

import android.widget.Button;

import android.widget.EditText;

import android.widget.TextView;

import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

private EditText usernameEditText, passwordEditText;
private TextView usernameTextView, passwordTextView;

private Button loginButton;

@Override

protected void onCreate(Bundle savedInstanceState) {

super.onCreate(savedInstanceState);

setContentView(R.layout.activity_main);

usernameEditText = findViewById(R.id.username_edit_text);

passwordEditText = findViewById(R.id.password_edit_text);

usernameTextView = findViewById(R.id.username_text_view);

passwordTextView = findViewById(R.id.password_text_view);

loginButton = findViewById(R.id.login_button);

usernameTextView.setText("Username:");

passwordTextView.setText("Password:");

loginButton.setOnClickListener(new View.OnClickListener() {

@Override

public void onClick(View v) {

String username = usernameEditText.getText().toString();

String password = passwordEditText.getText().toString();

// Login logic here

Toast.makeText(MainActivity.this, "Login successful!",

Toast.LENGTH_SHORT).show();

}

});

}

}

activity_main.xml

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"

android:layout_width="match_parent"

android:layout_height="match_parent"

android:orientation="vertical">

<TextView

android:id="@+id/username_text_view"

android:layout_width="match_parent"

android:layout_height="wrap_content" />

<EditText

android:id="@+id/username_edit_text"

android:layout_width="match_parent"

android:layout_height="wrap_content" />
<TextView

android:id="@+id/password_text_view"

android:layout_width="match_parent"

android:layout_height="wrap_content" />

<EditText

android:id="@+id/password_edit_text"

android:layout_width="match_parent"

android:layout_height="wrap_content"

android:inputType="textPassword" />

<Button

android:id="@+id/login_button"

android:layout_width="match_parent"

android:layout_height="wrap_content"

android:text="Login" />

</LinearLayout>
