# Installation
```
	npx create-expo-app blog --template blank
	npm install react-navigation
```

## Required React Navigation Installation Update
### 1. Install React Navigation
```
	npm install react-navigation@4.4.4 --legacy-peer-deps
```

### 2. Install Dependencies
```
	npx expo install react-native-gesture-handler react-native-reanimated react-native-screens react-native-safe-area-context @react-native-community/masked-view -- --legacy-peer-deps
```

### 3. Install React Navigation Stack
```
	npm install react-navigation-stack @react-native-community/masked-view --legacy-peer-deps
```

#### 4. Create a babel.config.js file
```
	module.exports = function (api) {
  api.cache(true);
  return {
    presets: ["babel-preset-expo"],
    plugins: ["react-native-reanimated/plugin"],
  };
};
```

##### Update Imports
```
	import { createAppContainer } from 'react-navigation';
	import { createStackNavigator } from 'react-navigation-stack';
```