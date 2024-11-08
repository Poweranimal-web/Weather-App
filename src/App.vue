<style>

/*
it's commited code for mobile anddroid app
*{
    margin: 0;
    padding: 0;
    margin-top: 10px;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #2E6582;
    color: white;
}

.topmenu {
  display: flex;
  align-items: flex-end;
  background-color: #132C46;
  padding: 10px;
  position: relative;
  white-space: nowrap; // Забезпечує горизонтальне розташування
}

.sities-container {
  flex: 1;
  overflow-x: hidden; // Вимикає горизонтальний скрол для користувачів
  white-space: nowrap; // Всі міста в одну лінію
  display: flex;
  align-items: center;
}

.sities {
    display: flex;
    justify-content: center;
    gap: 0px; // Відстань між містами
    flex-grow: 1; // Дозволяє містам займати ширину між іконками
    text-align: center;
    pointer-events: none;
}

.sities div {
    font-size: 12px;
    cursor: pointer;
    padding: 5px 10px; // Додаємо відступи для кожного міста
    margin: 1px 10px 1px 10px;
    border-radius: 10px; // Округлені краї
}

.sities div.active {
    background-color: #607ec7; // Колір фону для вибраного міста
    color: black; // Чорний текст для активного міста
    box-shadow: 0px 2px 8px 2px;
}

.sities .active {
  font-weight: bold;
  text-decoration: underline;
}

.bx {
  font-size: 30px;
  cursor: pointer;
}

#scrollLeft, #scrollRight {
  color: white;
}

.topmenu i {
    font-size: 25px; // Розмір іконок
    cursor: pointer;
    background-color: #132C46; // Фон під іконками
    padding: 0 2px 0 2px;
}

.maininf {
  padding: 10px 0 0 20px;
}

.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 20vh;
    margin-top: 30px;
  }

  .mtemperature {
    font-size: 50px;
    display: flex;
  }

  .condition {
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    margin-left: 30px;
    margin-top: 25px;
    font-size: 20px;
  }

  .mean-container {
    gap: 10px; // Проміжок між блоками
    align-items: center; // Вертикальне вирівнювання по центру
}

  .mean {
    padding-right: 9px;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    font-size: 14px;
  }

  .forecast {
    background-color: #132C46;
    border-radius: 20px;
    padding: 10px;
    display: flex;
    justify-content: space-around;
    width: 85%; // Задаємо ширину блоку на всю ширину viewport
    margin: 0; // Прибираємо будь-які відступи
  }

  .img-container{
    max-width: 100%; // Изображение не будет шире своего контейнера
    height: auto; // Сохраняет пропорции изображения
  }

  .forecast-item {
    width: 70px;
    font-size: 10px;
    text-align: center;
  }

  .forecast-block {

    background-color: #132C46;
    border-radius: 20px;
    padding: 20px;
    width: 90%; // Ширина блоку
    margin: 30px auto; // Центрування на сторінці
}

.forecast-day {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid rgba(255, 255, 255, 0.2); // Лінія між днями
}

.day-name {
  margin-right: 10px;
    font-size: 15px;
    font-weight: bold;
}

.weather-info {
    display: flex;
    align-items: center;
}

.weather-info .bx {
    font-size: 30px;
    margin-right: 30px; // Відступ між іконкою і температурою
}

.temperature {
    font-size: 15px;
    font-weight: bold;
}

.info-blocks {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 20px;
    padding: 50px 0 20px 0;
    width: 90%;
    margin: 0 auto; // Центрування на сторінці
}

.info-card {
  background-color: #0C2A42;
  border-radius: 15px; // Менший радіус для більшої компактності
  width: 47%; // Заповнює всю ширину для мобільного виду
  height: 120px; // Зменшена висота
  position: relative;
  padding: 10px 15px; // Зменшені відступи
  margin-bottom: 10px; // Відстань між картками
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.info-title {
  font-size: 24px; // Зменшено для більш компактного вигляду
  font-weight: normal;
  color: #B0C4DE; // Відтінок для кращого контрасту
}

.info-value {
  font-size: 25px;
  font-weight: bold;
  color: white; // Яскравий білий для показника
  margin: 0;
}

.info-value-veter{
  font-size: 25px;
  font-weight: bold;
  color: white; // Яскравий білий для показника
  margin: 0;
  align-items: flex-end;
}

.info-card i {
  position: absolute;
  top: 10px;
  right: 15px;
  font-size: 37px;
  color: #B0C4DE; // Світлий колір для іконки
}

.info-description {
  font-size: 11.5px;
  color: #B0C4DE; // Світлий відтінок для допоміжного тексту
  margin-top: 0;
}

// Стилі для модального вікна
.modal {
  display: none;
  position: fixed;
  z-index: 1;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal-content {
  background-color: #132C46;
  margin: 15% auto;
  padding: 20px;
  border-radius: 20px;
  width: 80%;
  height: 55%;
  max-width: 500px;
  color: white;
  text-align: center;
}

.close {
  color: white;
  float: right;
  font-size: 28px;
  font-weight: bold;
  cursor: pointer;
}

.close:hover,
.close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}

input#citySearch {
  width: 80%;
  padding: 10px;
  border-radius: 10px;
  border: none;
  margin-top: 20px;
}

button#searchCityBtn {
  padding: 10px 20px;
  background-color: #1D3547;
  color: white;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  margin-top: 10px;
}

button#searchCityBtn:hover {
  background-color: #0C2A42;
}*/
* {
    margin: 0;
    margin-top: 10px;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #2E6582;
    color: white;
}

.topmenu {
  display: flex;
  align-items: center;
  background-color: #132C46;
  padding: 10px;
  position: relative;
  white-space: nowrap; /* Забезпечує горизонтальне розташування */
}

.sities-container {
  flex: 1;
  overflow-x: hidden; /* Вимикає горизонтальний скрол для користувачів */
  white-space: nowrap; /* Всі міста в одну лінію */
  display: flex;
  align-items: center;
}

.sities {
    display: flex;
    justify-content: center;
    gap: 20px; /*Відстань між містами */
    flex-grow: 1; /*Дозволяє містам займати ширину між іконками */
    text-align: center;
    /* pointer-events: none; */
}

.sities div {
    font-size: 25px;
    cursor: pointer;
    padding: 5px 10px; /* Додаємо відступи для кожного міста*/
    margin: 1px 50px 1px 50px;
    border-radius: 10px; /* Округлені краї */
}

.sities div.active {
    background-color: #607ec7; /* Колір фону для вибраного міста*/
    color: black; /* Чорний текст для активного міста*/
    box-shadow: 0px 2px 8px 2px;
}

.sities div:hover {
    text-decoration: underline; /* Ефект при наведенні*/
}

.sities .active {
  font-weight: bold;
  text-decoration: underline;
}

.bx {
  font-size: 30px;
  cursor: pointer;
}

#scrollLeft, #scrollRight {
  color: white;
}

.topmenu i {
    font-size: 40px; /* Розмір іконок */
    cursor: pointer;
    background-color: #132C46; /* Фон під іконками */
    padding: 0 10px 0 10px;
}

.maininf {
  padding: 100px 0 0 100px;
}

.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 40vh;
  }
.mtemperature {
    font-size: 100px;
    display: flex;
  }
.condition {
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    margin-left: 70px;
    margin-top: 47px;
    font-size: 40px;
  }
.mean-container {
    display: flex; /* Горизонтальне розташування елементів */
    gap: 20px; /* Проміжок між блоками */
    align-items: center; /* Вертикальне вирівнювання по центру */
}
.mean {
    padding-right: 95px;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    font-size: 24px;
  }
.forecast {
    background-color: #132C46;
    border-radius: 20px;
    padding: 20px;
    display: flex;
    justify-content: space-around;
    width: 85%; /* Задаємо ширину блоку на всю ширину viewport */
    margin-top: 30px;
    margin-bottom: 30px;
  }
.forecast-item {
    font-size: 24px;
    text-align: center;
  }
.forecast-block {
    background-color: #132C46;
    border-radius: 20px;
    padding: 20px;
    width: 90%; /* Ширина блоку */
    margin: 40px auto; /* Центрування на сторінці */
}

.forecast-day {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 0;
    border-bottom: 1px solid rgba(255, 255, 255, 0.2); /* Лінія між днями */
}

.day-name {
    font-size: 30px;
    font-weight: bold;
}

.weather-info {
    display: flex;
    align-items: center;
}

.weather-info .bx {
    font-size: 40px;
    margin-right: 50px; /* Відступ між іконкою і температурою */
}

.temperature {
    font-size: 30px;
    font-weight: bold;
}

.info-blocks {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 20px;
    padding: 50px 0 20px 0;
    width: 90%;
    margin: 0 auto; /* Центрування на сторінці */
}

.info-card {
    background-color: #0C2A42;
    border-radius: 20px;
    width: 45%;
    height: 150px;
    position: relative;
    padding: 20px;
}

.info-title {
    position: absolute;
    top: 10px;
    left: 20px;
    font-size: 30px;
    font-weight: bold;
}

.info-value {
    position: absolute;
    bottom: 10px;
    left: 20px;
    font-size: 28px;
    font-weight: bold;
}

.info-card i {
    position: absolute;
    top: 10px;
    right: 20px;
    font-size: 70px;
}

.info-description {
  position: absolute;
  top: 50px;
  font-size: 20px;
}

/* Стилі для модального вікна */
.modal {
  display: none;
  position: fixed;
  z-index: 1;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal-content {
  background-color: #132C46;
  margin: 15% auto;
  padding: 20px;
  border-radius: 20px;
  width: 80%;
  height: 55%;
  max-width: 500px;
  color: white;
  text-align: center;
}

.close {
  color: white;
  float: right;
  font-size: 28px;
  font-weight: bold;
  cursor: pointer;
}

.close:hover,
.close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}

input#citySearch {
  width: 80%;
  padding: 10px;
  border-radius: 10px;
  border: none;
  margin-top: 20px;
  margin-bottom: 10px;
}

button#searchCityBtn {
  padding: 10px 20px;
  background-color: #1D3547;
  color: white;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  margin-top: 10px;
}

button#searchCityBtn:hover {
  background-color: #0C2A42;
}
.resultsContainer{
    display: none;
    flex-direction: column;
    overflow-y: scroll;
    width: 400px;
    height: 400px;
    margin: auto;
}
</style>
<script setup>
import { ref, computed } from 'vue'
import weatherName from './assets/descriptions.json'
const modal = ref(null)
const citiesPerSlide = 4
const currentSlide = ref(0)
const listPosition = ref([])
const hourlyWeather = ref([])
const dailyWeather = ref([])
const dataLocation = ref(null)
const dataWeather = ref(null)
const citySearchText = ref('')
const matchedResult = ref([])
const resultsContainer = ref(null)
let id = ref(getCookie('id') !== null ? JSON.parse(getCookie('id')) : 0)
const cityList = ref(getCookie('cities') !== null ? filterSavedCities(JSON.parse(getCookie('cities'))) : [])
const currentCityDetail = ref({ country: '', state: '' })
const appid = ref('5ecae512c05deedbe3b442ff6e4fb519')
console.log('dskdskdksdkskdskdj')
if (!navigator.geolocation) {
  console.error('Geolocation is not available.')
} else {
  console.log('Geolocation is available.')
}
const cityChunks = computed(() => {
  const chunks = []
  for (let i = 0; i < cityList.value.length; i += citiesPerSlide) {
    chunks.push(cityList.value.slice(i, i + citiesPerSlide))
  }
  return chunks
})
const maxSlide = computed(() => cityChunks.value.length - 1)

const nextSlide = () => {
  if (currentSlide.value < maxSlide.value) {
    currentSlide.value++
  }
}
function filterSavedCities (elements) {
  let array = elements
  for (let index = 0; index < array.length; index++) {
    if (array[index].active === true) {
      array[index].active = false
    }
  }
  return array
}
const prevSlide = () => {
  if (currentSlide.value > 0) {
    currentSlide.value--
  }
}
function openModal () {
  modal.value.style.display = 'block'
}
function closeModal () {
  modal.value.style.display = 'none'
}
function coverterToKm (visibility) {
  return Number(visibility) / 1000
}
function changeCity (city) {
  listPosition.value[0] = city.lat
  listPosition.value[1] = city.lon
  currentCityDetail.value.country = convertFullName(city.country)
  currentCityDetail.value.state = city.state
  clearWeatherData()
  getTempeturebyCity()
  findElementCity(city.id)
}
function findElementCity (id) {
  for (let i = 0; i < 9; i++) {
    if (cityList.value[i].id === id) {
      cityList.value[i].active = true
    } else {
      cityList.value[i].active = false
    }
  }
}
async function searchCity (event) {
  if (event.target.value.length > 0) {
    matchedResult.value = []
    const url = `https://api.openweathermap.org/geo/1.0/direct?q=${event.target.value}&limit=10&appid=${appid.value}`
    resultsContainer.value.style.display = 'flex'
    citySearchText.value = event.target.value
    let response = await fetch(url)
    response = await response.json()
    if (response.length > 0) {
      response.map((city, index) => {
        city.id = index
        matchedResult.value.push(city)
        return city
      })
    } else {
      console.log("It doesn't exist, input valid data")
    }
  } else {
    matchedResult.value = []
    resultsContainer.value.style.display = 'none'
    citySearchText.value = event.target.value
  }
}
function addCity (city) {
  let cityData = { id: id.value++, name: city.name, country: city.country, state: city.state, lat: city.lat, lon: city.lon, active: false }
  setCookie('id', id.value)
  cityList.value.push(cityData)
  const seenNames = new Set()
  cityList.value = cityList.value.filter(city => {
    if (seenNames.has(city.name) && seenNames.has(city.country) && seenNames.has(city.state)) {
      return false // Duplicate found, exclude it
    } else {
      seenNames.add(city.name) // Add new unique name to the Set
      seenNames.add(city.country)
      seenNames.add(city.state)
      return true // Keep this item
    }
  })
  setCookie('cities', JSON.stringify(cityList.value))
  matchedResult.value = []
  resultsContainer.value.style.display = 'none'
  citySearchText.value = ''
  closeModal()
  citySearchText.value = ''
  nextSlide()
}
async function getTempeture () {
  await getLocation()
  let cityData = { id: id.value++, name: dataLocation.value.address.city, country: dataLocation.value.address.country, state: dataLocation.value.address.state, lat: listPosition.value[0], lon: listPosition.value[1], active: true }
  currentCityDetail.value.country = dataLocation.value.address.country
  currentCityDetail.value.state = dataLocation.value.address.state
  cityList.value[0] = cityData
  console.log(cityList)
  callWeatherAPIByLocation()
  callWeatherAPIByHour()
  callWeatherAPIByDay()
}
function clearWeatherData () {
  hourlyWeather.value = []
  dailyWeather.value = []
  dataWeather.value = null
}
async function getTempeturebyCity () {
  callWeatherAPIByLocation()
  callWeatherAPIByHour()
  callWeatherAPIByDay()
}
function filterDate (date) {
  let options = { weekday: 'long' }
  if (date.getDate() === new Date().getDate()) {
    return 'Today'
  } else if (date.getDate() === new Date().getDate() + 1) {
    return 'Tomorrow'
  } else {
    return new Intl.DateTimeFormat('en-US', options).format(date)
  }
}
function filterTime (id, time) {
  if (id === 0) {
    return 'Now'
  } else {
    return `${new Date(time).getHours()}:00`
  }
}
function getWindDirection (d) {
// Insert the amount of degrees here
  let degrees = d

  // Define array of directions
  let directions = ['North', 'Northeast', 'East', 'Southeast', 'South', 'Southwest', 'West', 'Northwest']

  // Split into the 8 directions
  degrees = degrees * 8 / 360

  // round to nearest integer.
  degrees = Math.round(degrees, 0)

  // Ensure it's within 0-7
  degrees = (degrees + 8) % 8
  return directions[degrees]
}
async function callWeatherAPIByLocation () {
  const url = `https://api.openweathermap.org/data/2.5/weather?lat=${listPosition.value[0]}&lon=${listPosition.value[1]}&units=metric&appid=${appid.value}`
  const url2 = `https://api.open-meteo.com/v1/forecast?latitude=${listPosition.value[0]}&longitude=${listPosition.value[1]}&daily=temperature_2m_max,temperature_2m_min&timezone=auto&forecast_days=1&forecast_hours=6`
  const url3 = `https://api.open-meteo.com/v1/forecast?latitude=${listPosition.value[0]}&longitude=${listPosition.value[1]}&current=temperature_2m&forecast_days=1&forecast_hours=6`
  let response = await fetch(url)
  response = await response.json()
  let responseMaxMin = await fetch(url2)
  responseMaxMin = await responseMaxMin.json()
  let responseCurrentTemp = await fetch(url3)
  responseCurrentTemp = await responseCurrentTemp.json()
  response.main.temp = responseCurrentTemp.current.temperature_2m
  dataWeather.value = response.main
  dataWeather.value.temp_max = responseMaxMin.daily.temperature_2m_max[0]
  dataWeather.value.temp_min = responseMaxMin.daily.temperature_2m_min[0]
  dataWeather.value.visibility = response.visibility
  dataWeather.value.wind = response.wind
  dataWeather.value.description = response.weather[0].main
}
async function callWeatherAPIByHour () {
  const url = `https://api.open-meteo.com/v1/forecast?latitude=${listPosition.value[0]}&longitude=${listPosition.value[1]}&hourly=temperature_2m,weather_code&timezone=auto&forecast_days=1&forecast_hours=6`
  let response = await fetch(url)
  response = await response.json()
  for (let i = 0; i < 6; i++) {
    let weatherHourData = { id: i, weather: response.hourly.temperature_2m[i], time: response.hourly.time[i], weather_code: response.hourly.weather_code[i] }
    hourlyWeather.value.push(weatherHourData)
  }
}
async function callWeatherAPIByDay () {
  const url = `https://api.open-meteo.com/v1/forecast?latitude=${listPosition.value[0]}&longitude=${listPosition.value[1]}&daily=weather_code,temperature_2m_max,temperature_2m_min&timezone=auto&forecast_hours=6`
  let response = await fetch(url)
  response = await response.json()
  for (let i = 0; i < 6; i++) {
    let weatherDayData = { id: i, weather_max: response.daily.temperature_2m_max[i], weather_code: response.daily.weather_code[i], weather_min: response.daily.temperature_2m_min[i], date: response.daily.time[i] }
    dailyWeather.value.push(weatherDayData)
  }
}
// function getPosition () { // потрібно повернути значення довготи та широти з функції getCurrentPosition,для цього обернув її в Promise
//   return new Promise(function (resolve, reject) {
//     navigator.geolocation.getCurrentPosition(resolve, reject)
//   })
// }
async function getLocation () { // отримання даних містознаходження
  listPosition.value.push('48.4525768')
  listPosition.value.push('35.0710132')
  const url = `https://nominatim.openstreetmap.org/reverse.php?lat=${listPosition.value[0]}&lon=${listPosition.value[1]}&zoom=18&format=jsonv2`
  const response = await fetch(url)
  dataLocation.value = await response.json()
}
function downloadLink (code) {
  return weatherName[code].day.image
}
getTempeture()

window.onclick = function (event) {
  if (event.target === modal.value) {
    modal.value.style.display = 'none'
  }
}
function convertFullName (code) {
  if (code.length === 2) {
    let regionNames = new Intl.DisplayNames(['en'], { type: 'region' })
    return regionNames.of(code)
  } else {
    return code
  }
}
function deleteCity () {
  cityList.value = cityList.value.filter((city) => city.active !== true)
  cityList.value[0].active = true
  changeCity(cityList.value[0])
  setCookie('cities', JSON.stringify(cityList.value))
}
function setCookie (id, value) {
  document.cookie = id + '=' + value
}
function getCookie (id) {
  let value = document.cookie.match('(^|;)?' + id + '=([^;]*)(;|$)')
  return value ? unescape(value[2]) : null
}
</script>
<template>
  <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
    <title>Weather</title>
</head>
<body>
  <div class="topmenu">
    <i class='bx bx-chevron-left-circle' id="scrollLeft"  @click="prevSlide"></i>
    <i class='bx bx-minus' @click="deleteCity"></i>
    <div class="sities-container">
        <div class="sities" id="citiesList" v-for="(chunk, index) in cityChunks" :key="index" v-show="index === currentSlide">
            <div :class="{ active: city.active }" v-for="city in chunk" :key="city.id" @click="changeCity(city)">{{city.name}}</div>
        </div>
    </div>
    <i class='bx bx-plus' id="openModal" @click="openModal"></i>
    <i class='bx bx-chevron-right-circle' id="scrollRight" @click="nextSlide"></i>
  </div>

    <div id="myModal" class="modal" ref="modal">
      <div class="modal-content" >
          <span class="close" @click="closeModal">&times;</span>
          <h2>Search for City</h2>
          <input type="text" id="citySearch" placeholder="Enter city name..." :value="citySearchText" @input="searchCity"/>
          <div class="resultsContainer" ref="resultsContainer">
            <button v-for="result in matchedResult" :key="result.id" @click="addCity(result)" >{{ result.name }},{{ convertFullName(result.country) }}, {{ result.state }}</button>
          </div>
          <!-- <button id="searchCityBtn" @click="searchCity">Search</button> -->
      </div>
    </div>

      <div class="maininf">
        <div class="mtemperature">{{Math.round(Number(dataWeather.temp))}}°C <p class="condition">{{ dataWeather.description }}</p></div>
      <div class="mean-container">
        <div class="mean">AV {{Math.round(Number(dataWeather.temp_min))}}°C / {{Math.round(Number(dataWeather.temp_max))}}°C</div>
        <div class="mean">{{ currentCityDetail.country  }}, {{ currentCityDetail.state  }}</div>
      </div>
      </div>
    <div class="container">
        <div class="forecast">
          <div v-for="weather in hourlyWeather" v-bind:key="weather.id" class="forecast-item">
            <div>{{ filterTime(weather.id,weather.time) }}</div>
            <div><img class="img-container" v-bind:src="downloadLink(weather.weather_code)"/></div>
            <div>{{ new Date(weather.time).getHours() === new Date().getHours()? Math.round(Number(dataWeather.temp)) : Math.round(Number(weather.weather))  }}°C</div>
          </div>
          <!-- <div class="forecast-item">
            <div>16:00</div>
            <div>25</div>
          </div>
          <div class="forecast-item">
            <div>17:00</div>
            <div>26</div>
          </div>
          <div class="forecast-item">
            <div>18:00</div>
            <div>26</div>
          </div>
          <div class="forecast-item">
            <div>19:00</div>
            <div>26</div>
          </div>
          <div class="forecast-item">
            <div>20:00</div>
            <div>26</div>
          </div> -->
        </div>
      </div>
      <div class="forecast-block">
        <div v-for="weather in dailyWeather" :key="weather.id" class="forecast-day">
            <span class="day-name">{{filterDate(new Date(weather.date))}}</span>
            <div class="weather-info">
                <img v-bind:src="downloadLink(weather.weather_code)"/>
                <span class="temperature">{{Math.round(Number(weather.weather_min))}}°C/{{Math.round(Number(weather.weather_max))}}°C</span>
            </div>
        </div>
        <!-- <div class="forecast-day">
            <span class="day-name">Tomorrow</span>
            <div class="weather-info">
              <i class='bx bx-cloud-light-rain'></i>
                <span class="temperature">25/13</span>
            </div>
        </div>
        <div class="forecast-day">
            <span class="day-name">Monday</span>
            <div class="weather-info">
              <i class='bx bx-cloud-lightning'></i>
                <span class="temperature">25/13</span>
            </div>
        </div>
        <div class="forecast-day">
            <span class="day-name">Tuesday</span>
            <div class="weather-info">
                <i class='bx bx-sun'></i>
                <span class="temperature">25/13</span>
            </div>
        </div>
        <div class="forecast-day">
            <span class="day-name">Wednesday</span>
            <div class="weather-info">
                <i class='bx bx-sun'></i>
                <span class="temperature">25/13</span>
            </div>
        </div>
        <div class="forecast-day">
            <span class="day-name">Thursday</span>
            <div class="weather-info">
                <i class='bx bx-sun'></i>
                <span class="temperature">25/17</span>
            </div>
        </div> -->
    </div>
    <div class="info-blocks">
      <div class="info-card">
          <span class="info-title">Humidity</span>
          <i class='bx bx-droplet'></i>
          <span class="info-value">{{dataWeather.humidity}}%</span>
      </div>
      <div class="info-card">
          <span class="info-title">Wind</span>
          <span class="info-description">{{getWindDirection(dataWeather.wind.deg)}}</span>
          <i class='bx bx-wind'></i>
          <span class="info-value">{{Math.round(dataWeather.wind.speed)}} m/s</span>
      </div>
      <div class="info-card">
          <span class="info-title">Pressure</span>
          <i class='bx bx-water'></i>
          <span class="info-value">{{dataWeather.pressure}} hPa</span>
      </div>
      <div class="info-card">
          <span class="info-title">Visibility</span>
          <i class='bx bx-show-alt'></i>
          <span class="info-value">{{coverterToKm(dataWeather.visibility)}}km</span>
      </div>
  </div>
</body>
</html>
</template>
