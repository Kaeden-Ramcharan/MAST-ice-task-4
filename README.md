Readme - Mobile Application

# Album Collection & Debugging

**Developers**: Kaeden Ramcharan

**Student Numbers**: ST10525825

**Group**: 2

**Course**: MAST

**Subject**: Mobile App Scripting


## Links- 
**GitHub Repository**: https://github.com/Kaeden-Ramcharan/MAST-ice-task-4.git

---

## Project Overview - Introduction

The application contains weather information for three cities.

The user should be able to select a city and view the weather information associated with that city.

The supplied application contains hardcoded weather data. The purpose of the task is not to retrieve live weather information.
The application uses React Native state, objects, arrays, form inputs, validation, and FlatList.

The application was developed to meet the requirements of the assignment, which includes creating a functional mobile application and utilizing GitHub for version control and CI/CD automation using GitHub Actions.

---
## Development Environment


The following tools were used:

Expo

React Native

TypeScript

Institutional VM

BlueStacks 5

Expo Go

---

## 3. Error Log

The following errors were identified in the supplied `App.tsx`. Each entry
describes where the error occurred, what was wrong, why it affected the
application, and how it was corrected.

| # | Location | Problem | Error Type | Correction |
|---|---|---|---|---|
| 1 | Import statement | `ImageBackground` was used in the hero section of the JSX but was not imported from `react-native`. This caused a compile-time error and the application failed to start. | Import / Compile | Added `ImageBackground` to the list of imports from `react-native`. |
| 2 | City selector (3 places) | The selected-city comparison and the `onPress` handler used `weather.country` instead of `weather.city`. Because all three cities share the same country, no city ever matched the selected state, and clicking a button set the state to `'South Africa'`, which matched no entry. | Logic / State | Changed all three references from `weather.country` to `weather.city`. |
| 3 | Hourly forecast `.map()` | Each hourly card displayed `selectedWeather.temperature` (the current temperature) instead of the individual hour's temperature, so every card showed the same value. | Logic / Data | Changed to `hour.temperature`. |
| 4 | 5-day forecast `.map()` | The arrow function used a block body `{ }` without a `return` statement and contained a stray semicolon after `</View>`. As a result, no daily cards were rendered. | Syntax | Changed the block body to a parenthesised expression body `( ... )` and removed the stray semicolon. |
| 5 | 5-day forecast temperatures | The high temperature displayed `day.low` and the low temperature displayed `day.high`, so the values were swapped. | Logic / Data | Swapped the values so `highTemperature` uses `day.high` and `lowTemperature` uses `day.low`. |
| 6 | Sun & Moon section | The "Sunrise" row was passed `selectedWeather.sunset` instead of `selectedWeather.sunrise`, causing sunrise and sunset to display the same time. | Logic / Data | Changed the value to `selectedWeather.sunrise`. |
| 7 | `WeatherDetail` component | The value `<Text>` rendered `{label}` instead of `{value}`, so every detail row displayed its label twice and never displayed the actual data. | Logic | Changed `{label}` to `{value}` in the second `<Text>` element. |
| 8 | Current details – Humidity | The Humidity row was passed `selectedWeather.feelsLike` instead of `selectedWeather.humidity`, so humidity always matched the feels-like temperature. | Logic / Data | Changed to `selectedWeather.humidity`. |
| 9 | Hourly forecast `ScrollView` | The hourly `ScrollView` had `horizontal={false}`, causing the hourly cards to stack vertically instead of scrolling horizontally as intended. | Layout / Component Property | Changed to `horizontal={true}`. |
| 10 | `<ImageBackground>` source | `source` was passed a plain string, but React Native requires an object of the form `{ uri: ... }`. The background image therefore failed to render. | Runtime / Component Property | Changed to `source={{ uri: selectedWeather.backgroundImage }}`. |
| 11 | `dailyCard` style | `flexDirection: 'column'` contradicted the child styles, which use fixed widths and horizontal rows, indicating the card was intended to be a row. This broke the 5-day forecast layout. | Layout / Style | Changed to `flexDirection: 'row'` and added `alignItems: 'center'`. |
| 12 | `detailItem` style | `width: '100%'` forced every detail item onto its own line, collapsing the intended two-column grid into a single vertical column. | Layout / Style | Changed to `width: '48%'` so that two items fit per row. |

---

## App functionality

### Purpose:
The main purpose of this app is to view the weather for three different cities. 

### Key Features:

The dashboard should allow the user to view weather information for three different cities.

The application should present the weather information in a visually organised interface.

The supplied application will contain the data required to display the information.

---

## Design Considerations

The design of the Game Tester was based on the following key considerations:
1. **User Experience (UX)**: 
	The app was designed with the goal of providing an intuitive and easy-to-navigate user interface, ensuring a seamless user experience. 
2. **Responsiveness**: 
	The app was built to ensure it performs well on different screen sizes, with particular attention to device compatibility. 
3. **Simplicity**: 
	The design is minimalistic, focusing on core features without overwhelming the user. 
4. **Performance**: 
	Code optimization was considered to ensure fast response times and low battery usage.

---

## GitHub and GitHub Actions

This project was managed using GitHub for version control, where all code changes were committed and pushed regularly. GitHub enabled collaborative coding, allowing me to keep track of changes and maintain project integrity.

### GitHub Actions: 

I used GitHub actions to automate the build and deployment process. This includes: 
	
-Running tests to ensure the app's functionality.

-Compiling the app into APK files, which are the formats required for distribution.

-Uploading these build artifacts to GitHub for easy access.

---

## Screenshots of GitHub Change Log Commits

<img width="1806" height="696" alt="image" src="https://github.com/user-attachments/assets/196dd578-2069-42b1-a055-68c3fc88bd16" />
*Caption for screenshot 1: The changelog for 09 August 2026.*


## Screenshots of the code with errors

<img width="587" height="195" alt="image" src="https://github.com/user-attachments/assets/d4196278-8845-4f0a-9735-d738b38e5560" />
*Caption for screenshot 2: Error 1*


<img width="947" height="173" alt="image" src="https://github.com/user-attachments/assets/0905bb03-ff41-48ca-a84a-b4895170fa01" />
*Caption for screenshot 3: Error 2*


<img width="805" height="420" alt="image" src="https://github.com/user-attachments/assets/b564dc9e-0342-41d5-a837-d9613e9662fd" />
*Caption for screenshot 4: Error 3*


<img width="957" height="288" alt="image" src="https://github.com/user-attachments/assets/899bca39-7d28-405d-9138-9794806e7b9e" />
*Caption for screenshot 5: Error 4*

<img width="816" height="391" alt="image" src="https://github.com/user-attachments/assets/991abc10-612a-4441-86e7-c18e2e51e92e" />
*Caption for screenshot 6: Error 5*

## Screenshot of the app working

<img width="327" height="767" alt="image" src="https://github.com/user-attachments/assets/5ea3a05b-838f-41d7-8ed3-9e4472467970" />
*Caption for screenshot 6: Application running*

<img width="332" height="767" alt="image" src="https://github.com/user-attachments/assets/385cc6ee-0375-482a-848a-092506586ddb" />
*Caption for screenshot 7: Application running*

---

## References

1. [Reference 1: Google (2026) ReactNative [Computer program]. Available at: https://reactnative.dev/ (Accessed: 09 October 2026)]
2. [Reference 2: Google (2026) Expo [Computer program]. Available at: https://expo.dev/ (Accessed: 09 October 2026)]
3. [Reference 3: Google (2026) ExpoGo [Computer program]. Available at: https://expo.dev/go (Accessed: 09 October 2026)]

---

## AI Usage

I have used AI to help create the table in the readme document.

---


---
