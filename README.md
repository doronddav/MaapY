# MaapY
App for counting workouts on a map





## Description

This app build with Leaflet library.
The main purpose for this app is counting workouts,running and cycling, and mark them on a map.
The stracture of the app is foure classes, App,workout and two child class of the workout, Runing and Cycling.
This map will open on your current location. the root is to your latitude and longitude of your computer
```  const { latitude } = position.coords;
    const { longitude } = position.coords;
    const coords = [latitude, longitude];
    this.#map = L.map('map').setView(coords, (this.#mapZoomLevel = 13)); 
```

All data saved on Local Storage so the user can alwys see them untill he delete his localstorage.
``` _setLocalStorage() {
    localStorage.setItem('workouts', JSON.stringify(this.#workouts));
  }
  _getlocalStorage() {
    const data = JSON.parse(localStorage.getItem('workouts'));
    console.log(data);

    if (!data) return;

    this.#workouts = data;
    this.#workouts.forEach(work => {
      this._randerWorkout(work);
    });
  }
  ```

 



## How to use the Project
This app can be open just on live-server
```live-server``` on terminal.
To use this app click on the location you had your workout and fill in the form, first choose rinning or cycling and insert data.
if you had a workout far from your current location you can click the workout list on the workou's data and it will bring you to the bookmark.



