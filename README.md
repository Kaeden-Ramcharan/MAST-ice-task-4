Readme - Mobile Application

# Album Collection & Debugging

**Developers**: Kaeden Ramcharan

**Student Numbers**: ST10525825

**Group**: 2

**Course**: MAST

**Subject**: Mobile App Scripting


## Links- 
**GitHub Repository**: https://github.com/Kaeden-Ramcharan/MAST-ice-task-3.git

---

## Project Overview - Introduction

The application is intended to allow a user to:

Enter information about an album.

Validate the information entered.

Add the album to a favourites collection.

Display the albums in the collection.

Remove an album from the collection.

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
describes where the error occurs, what was wrong, why it was wrong, and how
it was corrected.

| # | Location | Problem | Error Type | Correction |
|---|---|---|---|---|
| 1 | `type Album` | `year` and `rating` were typed as `string`, but `handleSave` assigned `Number(year)` and `Number(rating)` to them. This produced a TypeScript type error and contradicted the intent of the fields. | TypeScript | Changed the type declarations to `year: number` and `rating: number`. |
| 2 | `<Picker>` – `selectedValue` | Bound to `title` instead of `genre`, so the picker reflected the title field rather than the selected genre. | Logic / State | Changed to `selectedValue={genre}`. |
| 3 | `<Picker.Item>` inside `genres.map` | Every item's `value` prop was set to `genre` (the state variable) instead of the current genre string, so selecting any option stored the wrong value. | Logic | Changed `value={genre}` to `value={item}`. |
| 4 | Import statement – `Picker` | Imported `Picker` from `@expo/ui/community/picker`, which is not the standard Expo picker package and is not included in the `expo-template-blank-typescript` template. | Import / Dependency | Installed and imported `Picker` from `@react-native-picker/picker` using `npx expo install @react-native-picker/picker`. |
| 5 | `<FlatList>` – `keyExtractor` | Used `item.title`, which is not guaranteed to be unique. Two albums with the same title would cause duplicate key warnings and rendering issues. | Runtime | Changed to `item.id`, which is unique. |

---

## App functionality

### Purpose:
The main purpose of this app is to record album information and rate the album. 

### Key Features:
The album record should contain appropriate information such as:

Album title

Artist

Year

Genre

Rating


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

<img width="1876" height="212" alt="image" src="https://github.com/user-attachments/assets/2ea4a042-b9e5-4910-b6f2-d38be9824e18" />
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

<img width="325" height="730" alt="image" src="https://github.com/user-attachments/assets/21e72ab3-b094-4368-acf2-9dc1f678390a" />
*Caption for screenshot 6: Application running*

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
