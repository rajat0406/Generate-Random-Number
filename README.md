# Generate-Random-Number
This project is good to start with Android Development.
This project consists of basic concepts used to start with Android:
# 1. Intent
An Intent is a messaging object you can use to request an action from another app component. Although intents facilitate communication between components in several ways, there are three fundamental use cases:

  # Starting an activity
  An Activity represents a single screen in an app. You can start a new instance of an Activity by passing an Intent to startActivity().     The Intent describes the activity to start and carries any necessary data.

  If you want to receive a result from the activity when it finishes, call startActivityForResult(). Your activity receives the result as   a separate Intent object in your activity's onActivityResult() callback. For more information, see the Activities guide.

  # Starting a service
  A Service is a component that performs operations in the background without a user interface. With Android 5.0 (API level 21) and later,   you can start a service with JobScheduler. For more information about JobScheduler, see its API-reference documentation.



  # Delivering a broadcast
  A broadcast is a message that any app can receive. The system delivers various broadcasts for system events, such as when the system       boots up or the device starts charging. You can deliver a broadcast to other apps by passing an Intent to sendBroadcast() or   sendOrderedBroadcast().

# 2. Button

  To display a button in an activity, add a button to the activity's layout XML file:

 <Button
     android:id="@+id/button_id"
     android:layout_height="wrap_content"
     android:layout_width="wrap_content"
     android:text="@string/self_destruct" />
To specify an action when the button is pressed, set a click listener on the button object in the corresponding activity code:

 public class MyActivity extends Activity {
     protected void onCreate(Bundle savedInstanceState) {
         super.onCreate(savedInstanceState);

         setContentView(R.layout.content_layout_id);

         final Button button = findViewById(R.id.button_id);
         button.setOnClickListener(new View.OnClickListener() {
             public void onClick(View v) {
                 // Code here executes on main thread after user presses button
             }
         });
     }
 }
The above snippet creates an instance of View.OnClickListener and wires the listener to the button using setOnClickListener(View.OnClickListener). As a result, the system executes the code you write in onClick(View) after the user presses the button.
