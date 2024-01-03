<!-- WeatherApp.svelte -->
<script>
  import { onMount } from 'svelte';
  import clearsky_day from '$lib/assets/clearsky_day.png';
  import clearsky_night from '$lib/assets/clearsky_night.png';
  import clearsky_polartwilight from '$lib/assets/clearsky_polartwilight.png';
  import cloudy from '$lib/assets/cloudy.png';
  import fair_day from '$lib/assets/fair_day.png';
  import fair_night from '$lib/assets/fair_night.png';
  import fair_polartwilight from '$lib/assets/fair_polartwilight.png';
  import fog from '$lib/assets/fog.png';
  import rain from '$lib/assets/rain.png';
  import heavyrain from '$lib/assets/heavyrain.png';
  import heavyrainandthunder from '$lib/assets/heavyrainandthunder.png';
  import heavyrainshowers_day from '$lib/assets/heavyrainshowers_day.png';
  import heavyrainshowers_night from '$lib/assets/heavyrainshowers_night.png';
  import heavyrainshowers_polartwilight from '$lib/assets/heavyrainshowers_polartwilight.png';
  import heavyrainshowersandthunder_day from '$lib/assets/heavyrainshowersandthunder_day.png';
  import heavyrainshowersandthunder_night from '$lib/assets/heavyrainshowersandthunder_night.png';
  import heavyrainshowersandthunder_polartwilight from '$lib/assets/heavyrainshowersandthunder_polartwilight.png';
  import heavysleet from '$lib/assets/heavysleet.png';
  import heavysleetandthunder from '$lib/assets/heavysleetandthunder.png';
  import heavysleetshowers_day from '$lib/assets/heavysleetshowers_day.png';
  import heavysleetshowers_night from '$lib/assets/heavysleetshowers_night.png';
  import heavysleetshowers_polartwilight from '$lib/assets/heavysleetshowers_polartwilight.png';
  import heavysleetshowersandthunder_day from '$lib/assets/heavysleetshowersandthunder_day.png';
  import heavysleetshowersandthunder_night from '$lib/assets/heavysleetshowersandthunder_night.png';
  import heavysleetshowersandthunder_polartwilight from '$lib/assets/heavysleetshowersandthunder_polartwilight.png';
  import heavysnow from '$lib/assets/heavysnow.png';
  import heavysnowandthunder from '$lib/assets/heavysnowandthunder.png';
  import heavysnowshowers_day from '$lib/assets/heavysnowshowers_day.png';
  import heavysnowshowers_night from '$lib/assets/heavysnowshowers_night.png';
  import heavysnowshowers_polartwilight from '$lib/assets/heavysnowshowers_polartwilight.png';
  import heavysnowshowersandthunder_day from '$lib/assets/heavysnowshowersandthunder_day.png';
  import heavysnowshowersandthunder_night from '$lib/assets/heavysnowshowersandthunder_night.png';
  import heavysnowshowersandthunder_polartwilight from '$lib/assets/heavysnowshowersandthunder_polartwilight.png';
  import lightrain from '$lib/assets/lightrain.png';
  import lightrainandthunder from '$lib/assets/lightrainandthunder.png';
  import lightrainshowers_day from '$lib/assets/lightrainshowers_day.png';
  import lightrainshowers_night from '$lib/assets/lightrainshowers_night.png';
  import lightrainshowers_polartwilight from '$lib/assets/lightrainshowers_polartwilight.png';
  import lightrainshowersandthunder_day from '$lib/assets/lightrainshowersandthunder_day.png';
  import lightrainshowersandthunder_night from '$lib/assets/lightrainshowersandthunder_night.png';
  import lightrainshowersandthunder_polartwilight from '$lib/assets/lightrainshowersandthunder_polartwilight.png';
  import lightsleet from '$lib/assets/lightsleet.png';
  import lightsleetandthunder from '$lib/assets/lightsleetandthunder.png';
  import lightsleetshowers_day from '$lib/assets/lightsleetshowers_day.png';
  import lightsleetshowers_night from '$lib/assets/lightsleetshowers_night.png';
  import lightsleetshowers_polartwilight from '$lib/assets/lightsleetshowers_polartwilight.png';
  import lightsnow from '$lib/assets/lightsnow.png';
  import lightsnowandthunder from '$lib/assets/lightsnowandthunder.png';
  import lightsnowshowers_day from '$lib/assets/lightsnowshowers_day.png';
  import lightsnowshowers_night from '$lib/assets/lightsnowshowers_night.png';
  import lightsnowshowers_polartwilight from '$lib/assets/lightsnowshowers_polartwilight.png';
  import lightsleetshowersandthunder_day from '$lib/assets/lightsleetshowersandthunder_day.png';
  import lightsleetshowersandthunder_night from '$lib/assets/lightsleetshowersandthunder_night.png';
  import lightsleetshowersandthunder_polartwilight from '$lib/assets/lightsleetshowersandthunder_polartwilight.png';
  import lightsnowshowersandthunder_day from '$lib/assets/lightsnowshowersandthunder_day.png';
  import lightsnowshowersandthunder_night from '$lib/assets/lightsnowshowersandthunder_night.png';
  import lightsnowshowersandthunder_polartwilight from '$lib/assets/lightsnowshowersandthunder_polartwilight.png';
  import partlycloudy_day from '$lib/assets/partlycloudy_day.png';
  import partlycloudy_night from '$lib/assets/partlycloudy_night.png';
  import partlycloudy_polartwilight from '$lib/assets/partlycloudy_polartwilight.png';
  import rainandthunder from '$lib/assets/rainandthunder.png';
  import rainshowers_day from '$lib/assets/rainshowers_day.png';
  import rainshowers_night from '$lib/assets/rainshowers_night.png';
  import rainshowers_polartwilight from '$lib/assets/rainshowers_polartwilight.png';
  import rainshowersandthunder_day from '$lib/assets/rainshowersandthunder_day.png';
  import rainshowersandthunder_night from '$lib/assets/rainshowersandthunder_night.png';
  import rainshowersandthunder_polartwilight from '$lib/assets/rainshowersandthunder_polartwilight.png';
  import sleet from '$lib/assets/sleet.png';
  import sleetandthunder from '$lib/assets/sleetandthunder.png';
  import sleetshowers_day from '$lib/assets/sleetshowers_day.png';
  import sleetshowers_night from '$lib/assets/sleetshowers_night.png';
  import sleetshowers_polartwilight from '$lib/assets/sleetshowers_polartwilight.png';
  import sleetshowersandthunder_day from '$lib/assets/sleetshowersandthunder_day.png';
  import sleetshowersandthunder_night from '$lib/assets/sleetshowersandthunder_night.png';
  import sleetshowersandthunder_polartwilight from '$lib/assets/sleetshowersandthunder_polartwilight.png';
  import snow from '$lib/assets/snow.png';
  import snowandthunder from '$lib/assets/snowandthunder.png';
  import snowshowers_day from '$lib/assets/snowshowers_day.png';
  import snowshowers_night from '$lib/assets/snowshowers_night.png';
  import snowshowers_polartwilight from '$lib/assets/snowshowers_polartwilight.png';
  import snowshowersandthunder_day from '$lib/assets/snowshowersandthunder_day.png';
  import snowshowersandthunder_night from '$lib/assets/snowshowersandthunder_night.png';
  import snowshowersandthunder_polartwilight from '$lib/assets/snowshowersandthunder_polartwilight.png';

  let address = '';
  let latitude = null;
  let longitude = null;
  let weatherData = null;
  let timedata = '';
  let backgroundImageUrl = '';
  const apiKey = 'AIzaSyDrcBMJDq3KN3zibV3v5D2n5mhBNJDF9Sc';
  const fetchgooglesearchdata = async () => {
  const googlesearchurl = `https://www.googleapis.com/customsearch/v1?q=${address}&searchType=image&key=AIzaSyDrcBMJDq3KN3zibV3v5D2n5mhBNJDF9Sc&cx=52ae0b110a2124e55`;
  try {
  const searchresponse = await fetch(googlesearchurl);
  const searchdata = await searchresponse.json();

  if (searchdata.items && searchdata.items.length > 0) {
    backgroundImageUrl = searchdata.items[0].link;
  }
} catch (error) {
  console.error('Error fetching Google search data:', error);
}
  }

  const fetchGeocodingData = async () => {
    const geoUrl = `https://maps.googleapis.com/maps/api/geocode/json?address=${address}&key=${apiKey}`;
  
    try {
      const response = await fetch(geoUrl);
      const data = await response.json();

      if (data.status === 'OK' && data.results.length > 0) {
        const result = data.results[0];
        address = result.formatted_address;
        latitude = result.geometry.location.lat;
        longitude = result.geometry.location.lng;

        await fetchWeatherData();
        await fetchTimeData();
      } else {
        console.error('Geocoding API request failed:', data.status);
      }
    } catch (error) {
      console.error('Error fetching geocoding data:', error);
    }
  };

  const fetchWeatherData = async () => {
    const weatherUrl = `https://api.met.no/weatherapi/locationforecast/2.0/compact?lat=${latitude}&lon=${longitude}`;

    try {
      const weatherResponse = await fetch(weatherUrl);
      weatherData = await weatherResponse.json();
    } catch (error) {
      console.error('Error fetching weather data:', error);
    }
  };
  const fetchTimeData = async () => {
  const timestamp = Math.floor(Date.now() / 1000);
  const timeUrl = `https://maps.googleapis.com/maps/api/timezone/json?location=${latitude},${longitude}&timestamp=${timestamp}&key=${apiKey}`;

  try {
    const timeResponse = await fetch(timeUrl);
    timedata = await timeResponse.json();

    // Calculate the current time in the fetched time zone
    const date = new Date();
    const utcTime = date.getTime() + date.getTimezoneOffset() * 60000;
    const localTime = new Date(utcTime + 1000 * timedata.rawOffset + 1000 * timedata.dstOffset);
    timedata.localTime = localTime.toLocaleString();
  } catch (error) {
    console.error('Error fetching time data:', error);
  }
};

const fetchAllData = async () => {
    await fetchgooglesearchdata();
    await fetchGeocodingData();
  };
onMount(() => {
  setInterval(fetchAllData, 3600000); // Fetch data every hour
});


</script>
<body class="max-h-screen w-screen bg-cover bg-scroll bg-opacity-10 " style="background-image: url('{backgroundImageUrl}')">
  <main class="text-center text-red-500 ">
    <div class="content">

  <h1 class="text-9xl font-bold underline">Weather App</h1>
  <form on:submit|preventDefault={fetchAllData} class="mt-4">
    <label for="address" class="block">Address:</label>
    <input type="text" id="address" bind:value={address} class="border p-2" />
    <button type="submit" class="mt-0 bg-blue-500 text-white p-2 rounded">Get Weather</button>
  </form>

      <div class="box1 w-1/2 mx-auto h-full rounded-full text-center border-transparent">
        {#if address && latitude !== null && longitude !== null && weatherData}
          <!-- Other content -->
          <h2 class="mt-0">Location Information</h2>
      
          <p class="mb-0"><strong>Address:</strong> {address}</p>
          <p class="mb-0"><strong>Timezone Name:</strong> {timedata.timeZoneName}</p>
          <p class="mb-0"><strong>Latitude:</strong> {latitude}</p>
          <p class="mb-0"><strong>Longitude:</strong> {longitude}</p>
  
          <h2>Weather Data</h2>
          <div class="bg-right-top">
            {#each weatherData.properties.timeseries as { time,data}}
              <div class="mb-0 flex-col text-center rounded-xl box-border p-4 border-4 border-blue-300">
              <p class="mb-0"><strong>{address} time:</strong> {timedata.localTime}</p>
              <p><strong>Air Temperature:</strong> {data.instant.details.air_temperature} °C</p>
              {#if data.next_1_hours && data.next_1_hours.summary}
                <p><strong>Next 1 Hour Symbol Code:</strong> {data.next_1_hours.summary.symbol_code}</p>
    
                                  
                  {#if data.next_1_hours.summary.symbol_code === 'clearsky_day'}
                  <img src={clearsky_day} alt="Clear Sky Day" />
                  {:else if data.next_1_hours.summary.symbol_code === 'clearsky_night'}
                  <img src={clearsky_night} alt="Clear Sky Night" />
                  {:else if data.next_1_hours.summary.symbol_code === 'clearsky_polartwilight'}
                  <img src={clearsky_polartwilight} alt="Clear Sky Polar Twilight" />
                  {:else if data.next_1_hours.summary.symbol_code === 'cloudy'}
                  <img src={cloudy} alt="Cloudy" />
                  {:else if data.next_1_hours.summary.symbol_code === 'fair_day'}
                  <img src={fair_day} alt="Fair Day" />
                  {:else if data.next_1_hours.summary.symbol_code === 'fair_night'}
                  <img src={fair_night} alt="Fair Night" />
                  {:else if data.next_1_hours.summary.symbol_code === 'fair_polartwilight'}
                  <img src={fair_polartwilight} alt="Fair Polar Twilight" />
                  {:else if data.next_1_hours.summary.symbol_code === 'fog'}
                  <img src={fog} alt="Fog" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavyrain'}
                  <img src={heavyrain} alt="Heavy Rain" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavyrainandthunder'}
                  <img src={heavyrainandthunder} alt="Heavy Rain and Thunder" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavyrainshowers_day'}
                  <img src={heavyrainshowers_day} alt="Heavy Rain Showers Day" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavyrainshowers_night'}
                  <img src={heavyrainshowers_night} alt="Heavy Rain Showers Night" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavyrainshowers_polartwilight'}
                  <img src={heavyrainshowers_polartwilight} alt="Heavy Rain Showers Polar Twilight" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavyrainshowersandthunder_day'}
                  <img src={heavyrainshowersandthunder_day} alt="Heavy Rain Showers and Thunder Day" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavyrainshowersandthunder_night'}
                  <img src={heavyrainshowersandthunder_night} alt="Heavy Rain Showers and Thunder Night" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavyrainshowersandthunder_polartwilight'}
                  <img src={heavyrainshowersandthunder_polartwilight} alt="Heavy Rain Showers and Thunder Polar Twilight" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysleet'}
                  <img src={heavysleet} alt="Heavy Sleet" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysleetandthunder'}
                  <img src={heavysleetandthunder} alt="Heavy Sleet and Thunder" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysleetshowers_day'}
                  <img src={heavysleetshowers_day} alt="Heavy Sleet Showers Day" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysleetshowers_night'}
                  <img src={heavysleetshowers_night} alt="Heavy Sleet Showers Night" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysleetshowers_polartwilight'}
                  <img src={heavysleetshowers_polartwilight} alt="Heavy Sleet Showers Polar Twilight" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysleetshowersandthunder_day'}
                  <img src={heavysleetshowersandthunder_day} alt="Heavy Sleet Showers and Thunder Day" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysleetshowersandthunder_night'}
                  <img src={heavysleetshowersandthunder_night} alt="Heavy Sleet Showers and Thunder Night" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysleetshowersandthunder_polartwilight'}
                  <img src={heavysleetshowersandthunder_polartwilight} alt="Heavy Sleet Showers and Thunder Polar Twilight" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysnow'}
                  <img src={heavysnow} alt="Heavy Snow" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysnowandthunder'}
                  <img src={heavysnowandthunder} alt="Heavy Snow and Thunder" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysnowshowers_day'}
                  <img src={heavysnowshowers_day} alt="Heavy Snow Showers Day" />
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysnowshowers_night'}
                  <img src={heavysnowshowers_night} alt="Heavy Snow Showers Night" />               
                  {:else if data.next_1_hours.summary.symbol_code === 'heavysnowshowers_polartwilight'}
                  <img src={heavysnowshowers_polartwilight} alt="Heavy Snow Showers Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'heavysnowshowersandthunder_day'}
                  <img src={heavysnowshowersandthunder_day} alt="Heavy Snow Showers and Thunder Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'heavysnowshowersandthunder_night'}
                  <img src={heavysnowshowersandthunder_night} alt="Heavy Snow Showers and Thunder Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'heavysnowshowersandthunder_polartwilight'}
                  <img src={heavysnowshowersandthunder_polartwilight} alt="Heavy Snow Showers and Thunder Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightrain'}
                  <img src={lightrain} alt="Light Rain" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightrainandthunder'}
                  <img src={lightrainandthunder} alt="Light Rain and Thunder" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightrainshowers_day'}
                  <img src={lightrainshowers_day} alt="Light Rain Showers Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightrainshowers_night'}
                  <img src={lightrainshowers_night} alt="Light Rain Showers Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightrainshowers_polartwilight'}
                  <img src={lightrainshowers_polartwilight} alt="Light Rain Showers Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightrainshowersandthunder_day'}
                  <img src={lightrainshowersandthunder_day} alt="Light Rain Showers and Thunder Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightrainshowersandthunder_night'}
                  <img src={lightrainshowersandthunder_night} alt="Light Rain Showers and Thunder Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightrainshowersandthunder_polartwilight'}
                  <img src={lightrainshowersandthunder_polartwilight} alt="Light Rain Showers and Thunder Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsleet'}
                  <img src={lightsleet} alt="Light Sleet" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsleetandthunder'}
                  <img src={lightsleetandthunder} alt="Light Sleet and Thunder" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsleetshowers_day'}
                  <img src={lightsleetshowers_day} alt="Light Sleet Showers Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsleetshowers_night'}
                  <img src={lightsleetshowers_night} alt="Light Sleet Showers Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsleetshowers_polartwilight'}
                  <img src={lightsleetshowers_polartwilight} alt="Light Sleet Showers Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsnow'}
                  <img src={lightsnow} alt="Light Snow" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsnowandthunder'}
                  <img src={lightsnowandthunder} alt="Light Snow and Thunder" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsnowshowers_day'}
                  <img src={lightsnowshowers_day} alt="Light Snow Showers Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsnowshowers_night'}
                  <img src={lightsnowshowers_night} alt="Light Snow Showers Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsnowshowers_polartwilight'}
                  <img src={lightsnowshowers_polartwilight} alt="Light Snow Showers Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsleetshowersandthunder_day'}
                  <img src={lightsleetshowersandthunder_day} alt="Light Sleet Showers and Thunder Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsleetshowersandthunder_night'}
                  <img src={lightsleetshowersandthunder_night} alt="Light Sleet Showers and Thunder Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsleetshowersandthunder_polartwilight'}
                  <img src={lightsleetshowersandthunder_polartwilight} alt="Light Sleet Showers and Thunder Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsnowshowersandthunder_day'}
                  <img src={lightsnowshowersandthunder_day} alt="Light Snow Showers and Thunder Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsnowshowersandthunder_night'}
                  <img src={lightsnowshowersandthunder_night} alt="Light Snow Showers and Thunder Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'lightsnowshowersandthunder_polartwilight'}
                  <img src={lightsnowshowersandthunder_polartwilight} alt="Light Snow Showers and Thunder Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'partlycloudy_day'}
                  <img src={partlycloudy_day} alt="Partly Cloudy Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'partlycloudy_night'}
                  <img src={partlycloudy_night} alt="Partly Cloudy Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'partlycloudy_polartwilight'}
                  <img src={partlycloudy_polartwilight} alt="Partly Cloudy Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'rainandthunder'}
                  <img src={rainandthunder} alt="Rain and Thunder" />
                {:else if data.next_1_hours.summary.symbol_code === 'rainshowers_day'}
                  <img src={rainshowers_day} alt="Rain Showers Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'rainshowers_night'}
                  <img src={rainshowers_night} alt="Rain Showers Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'rainshowers_polartwilight'}
                  <img src={rainshowers_polartwilight} alt="Rain Showers Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'rainshowersandthunder_day'}
                  <img src={rainshowersandthunder_day} alt="Rain Showers and Thunder Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'rainshowersandthunder_night'}
                  <img src={rainshowersandthunder_night} alt="Rain Showers and Thunder Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'rainshowersandthunder_polartwilight'}
                  <img src={rainshowersandthunder_polartwilight} alt="Rain Showers and Thunder Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'sleet'}
                  <img src={sleet} alt="Sleet" />
                {:else if data.next_1_hours.summary.symbol_code === 'sleetandthunder'}
                  <img src={sleetandthunder} alt="Sleet and Thunder" />
                {:else if data.next_1_hours.summary.symbol_code === 'sleetshowers_day'}
                  <img src={sleetshowers_day} alt="Sleet Showers Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'sleetshowers_night'}
                  <img src={sleetshowers_night} alt="Sleet Showers Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'sleetshowers_polartwilight'}
                  <img src={sleetshowers_polartwilight} alt="Sleet Showers Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'sleetshowersandthunder_day'}
                  <img src={sleetshowersandthunder_day} alt="Sleet Showers and Thunder Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'sleetshowersandthunder_night'}
                  <img src={sleetshowersandthunder_night} alt="Sleet Showers and Thunder Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'sleetshowersandthunder_polartwilight'}
                  <img src={sleetshowersandthunder_polartwilight} alt="Sleet Showers and Thunder Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'snowandthunder'}
                  <img src={snowandthunder} alt="Snow and Thunder" />
                {:else if data.next_1_hours.summary.symbol_code === 'snowshowers_day'}
                  <img src={snowshowers_day} alt="Snow Showers Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'snowshowers_night'}
                  <img src={snowshowers_night} alt="Snow Showers Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'snowshowers_polartwilight'}
                  <img src={snowshowers_polartwilight} alt="Snow Showers Polar Twilight" />
                {:else if data.next_1_hours.summary.symbol_code === 'snowshowersandthunder_day'}
                  <img src={snowshowersandthunder_day} alt="Snow Showers and Thunder Day" />
                {:else if data.next_1_hours.summary.symbol_code === 'snowshowersandthunder_night'}
                  <img src={snowshowersandthunder_night} alt="Snow Showers and Thunder Night" />
                {:else if data.next_1_hours.summary.symbol_code === 'snowshowersandthunder_polartwilight'}
                  <img src={snowshowersandthunder_polartwilight} alt="Snow Showers and Thunder Polar Twilight" />
                  {:else if data.next_1_hours.summary.symbol_code === 'snow'}
                  <img src={snow} alt="Snow Showers and Thunder Polar Twilight" />
                  {:else if data.next_1_hours.summary.symbol_code === 'rain'}
                  <img src={rain} alt="rain" />
                {/if}   
                {/if}
              </div>
            {/each}
          </div>
        {/if}
      </div>
    </div>
  </main>
</body>
