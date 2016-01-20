# snippets
snippets


Sharedpreferences

SharedPreferences  mPrefs = getPreferences(MODE_PRIVATE);
#For save
        Editor prefsEditor = mPrefs.edit();
        Gson gson = new Gson();
        String json = gson.toJson(MyObject);
        prefsEditor.putString("MyObject", json);
        prefsEditor.commit();
#For get
    Gson gson = new Gson();
    String json = mPrefs.getString("MyObject", "");
    MyObject obj = gson.fromJson(json, MyObject.class);
