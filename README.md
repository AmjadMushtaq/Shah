   In static class method we can call to the multiple screen  with the help of Boolean Variables. The 
Below is the code of  Boolean. this we used in main activity where we go to the another screens.
   
   
   static class Amjad {

        public static Boolean aBoolean=false;
    }

 


    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);


        if(Tiger.aBoolean){
           Toast.makeText(this,"Hello",Toast.LENGTH_SHORT).show();
            Tiger.aBoolean=false;
        }else{

        }

 These are the code in one activity .
 ...............................................................................................................................

                This is other activity code where we come back to the that screen which we give the name of the activity 
                
                
                    TextView textView2;    <<<<<------------------- Create Variable




    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_profile_acitivity);
        MainActivity.Tiger.aBoolean=true;  <<<<<<<------------------------------------- Main Activity
      
        textView2=findViewById(R.id.textView2);  <--------------<<<--------------   apply setOnclicklisnear

        textView2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent i=new Intent(ProfileAcitivity.this,MainActivity.class);
                startActivity(i);
            }
        });
