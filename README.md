2.AIM:Create an application that takes the name from a text box and shows hello
message along with the name entered in text box, when the user clicks the OK
button
XML CODE:
<?xml version="1.0" encoding="utf-8"?>
<LinearLayoutxmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:orientation="vertical"
android:gravity="center"
tools:context=".MainActivity">
<LinearLayout
android:layout_width="wrap_content"
android:layout_height="wrap_content">
<EditText
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:id="@+id/edtname"
android:hint="Enter your name"
android:inputType="text"
 />
<Button
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginLeft="11dp"
4 | P a g e
android:id="@+id/btnok"
android:backgroundTint="#182985"
android:textColor="#fff"
android:text="OK"
android:textStyle="bold"
>
</Button>
</LinearLayout>
<TextView
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:id="@+id/txtview"
android:textSize="25sp"
android:textStyle="bold"
android:textColor="#0F1D97"
android:layout_marginTop="30dp">
</TextView>
</LinearLayout>
JAVA CODE:
package com.example.csbs02;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import org.w3c.dom.Text;
public class MainActivity extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 Button btnok = findViewById(R.id.btnok);
TextViewtxtview = findViewById(R.id.txtview);
 EditText edname = findViewById(R.id.edtname);
btnok.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View view) {
 String str = edname.getText().toString();
txtview.setText("Hi " +str);
 }
 });
 }
6 | P a g e
}
