# React Native

- Fundamental Concepts

  - View Component
    - Text Component
    - Image Component
      ![Image](Images/image.png)
    - Button Component
      ![Button](Images/image-1.png)
    - TouchableOpacity Component
      ![TouchableOpacity](Images/image-2.png)
      ![OnPress](Images/image-3.png)
      ![TouchableHighlight](Images/image-4.png)
    - Pressable Component
      ![Pressable](Images/image-5.png)
    - SafeAreaView Component
      ![SafeAreaView](Images/image-6.png)

- Styling
  Same as CSS but uses camelCase
  ![Styling](Images/image-7.png)
  Passing as an object
  ![PassingAsObject](Images/image-8.png)

  - StyleSheet
    ![StyleSheet](Images/image-9.png)
    ![StyleSheet2](Images/image-10.png)
    ![StyleSheet3](Images/image-11.png)
    ![alt text](Images/image-12.png)
    ![alt text](Images/image-13.png)
    ![alt text](Images/image-14.png)
    Don't use javascript objects for styles because it creates a new object on every render
    Instead use StyleSheet.create
    It loads only once
    For dynamic css we can use inline styles
    like onPress we can change the background color,etc
    Both combination of StyleSheet and inline styles works
  - Theme-based styling
    ![Theme-based styling](Images/image-15.png)
    ![Theme-based styling2](Images/image-16.png)
  - Use percentage as units
    ![Percentage](Images/image-17.png)
  - Flexbox
    Flex helps us to divide the space
    ![alt text](Images/image-18.png)
    ![alt text](Images/image-19.png)
    ![alt text](Images/image-20.png)
    ![alt text](Images/image-21.png)
    ![alt text](Images/image-22.png)
  - Flex Direction
    ByDefault it is vertical
    ![alt text](Images/image-23.png)
    ![alt text](Images/image-24.png)
    ![alt text](Images/image-25.png)
  - Align Items and Justify Content
    ![alt text](Images/image-26.png)
    ![alt text](Images/image-27.png)
    ![alt text](Images/image-28.png)
    ![alt text](Images/image-29.png)
    ![alt text](Images/image-30.png)
  - Align Self
    ![alt text](Images/image-31.png)
  - Wrapping
    ![alt text](Images/image-32.png)
    ![alt text](Images/image-33.png)
    ![alt text](Images/image-34.png)
    ![alt text](Images/image-35.png)
    When flexWrap is set to wrap the align items works on lines and doesn't work properly
    So to center the items we can use alignContent on the parent container
    ![alt text](Images/image-36.png)
    ![alt text](Images/image-37.png)
  - Flex Grow
    If you assign flexGrow: 1 to a component, it will take up all the available space in its container.
    ![alt text](Images/image-38.png)
    Works similarly to flex: 1
  - Flex Shrink
    If you assign flexShrink: 1 to a component, it will shrink to fit within its container if there is not enough space.
  - Flex Basis
    If you assign flexBasis: 100 to a component, it will take up 100 pixels of space in its container.

- ScrollView
  To make the content scrollable
  ![ScrollView](Images/image-39.png)
  Also styling is different for ScrollView
  ![ScrollView2](Images/image-40.png)
  ![ScrollView3](Images/image-41.png)
- FlatList
  For large lists of data
  More efficient than ScrollView
  ![FlatList](Images/image-42.png)
  ![FlatList2](Images/image-43.png)
  Styling
  ![FlatList3](Images/image-44.png)
  Props
  ![FlatList4](Images/image-45.png)
  ![ColumnWrapperStyle](Images/image-46.png)
  FlatList benefit over ScrollView is it only renders the items that are visible on the screen
  So it is more efficient for large lists of data
  extraData is used to re-render the list when the data changes
  ![extraData](Images/image-47.png)
  ![horizontal](Images/image-48.png)

- Handling User Input

  - TextInput
    ![TextInput](Images/image-49.png)
    ![TextInput2](Images/image-50.png)
    ![TextInput3](Images/image-51.png)
    ![WholeCode](Images/image-52.png)
    New Way to write onChangeText
    ![NewOnChangeText](Images/image-52.png)
  - Properties
    ![TextInputProperties](Images/image-53.png)
    More Properties
    [Documentation](https://reactnative.dev/docs/textInput)
    ![TextInput4](Images/image-54.png)
  - Keyboard Types
    ![KeyboardTypes](Images/image-55.png)
    [Documentation](https://reactnative.dev/docs/textInput#keyboardtype)

- Navigation
  We can use react-navigation library for navigation
- Stack Navigation
  For example a login screen and a home screen
  We can navigate between them using stack navigation
  [Stack Navigation](https://reactnavigation.org/docs/native-stack-navigator/)
- Tab Navigation
  For example a home screen with multiple tabs like home, profile, settings
  We can navigate between them using tab navigation
  [Tab Navigation](https://reactnavigation.org/docs/bottom-tab-navigator/)
- Drawer Navigation
  For example a home screen with a drawer menu
  [Drawer Navigation](https://reactnavigation.org/docs/drawer-navigator/)
- React Navigation Docs
  [Docs](https://reactnavigation.org/docs/getting-started/)
  ![Stack Navigation](Images/image-56.png)
  ![Stack Navigation](Images/image-57.png)
  ![alt text](Images/image-58.png)
  ![alt text](Images/image-59.png)
  ![alt text](Images/image-60.png)
  ![alt text](Images/image-61.png)
  ![alt text](Images/image-62.png)
- Props
  ![alt text](Images/image-63.png)
  ![alt text](Images/image-64.png)
  Top page will have no back button and will render first
  ![alt text](Images/image-65.png)
  Also one property to set initialRouteName
  ![alt text](Images/image-66.png)
  More properties
  ![alt text](Images/image-67.png)
  [More Options](https://reactnavigation.org/docs/native-stack-navigator/#options)
  ![alt text](Images/image-68.png)
  You can apply one option globally to all screens in the navigator with the screenOptions prop on the Stack.Navigator
  ![alt text](Images/image-69.png)
  Global options can be overridden on a per-screen basis by specifying options on the individual screen.
  Stack Navigation helpers like navigation.navigate, navigation.push, navigation.pop, navigation.popToTop, navigation.replace, navigation.reset
  [Docs](https://reactnavigation.org/docs/native-stack-navigator/#helpers)
  Performs like stack data structure
- - Tab Navigator
    Similar to stack navigator but with tabs at the bottom
    ![alt text](Images/image-70.png)
    ![alt text](Images/image-71.png)
    ![alt text](Images/image-72.png)
    ![alt text](Images/image-73.png)
    Bottom tab is ready to use with createBottomTabNavigator you can do styling with your own
    ![alt text](Images/image-74.png)
    Some important properties:
    ![alt text](Images/image-75.png)
    ![alt text](Images/image-76.png)
    ![alt text](Images/image-77.png)
    Global styling for tab navigator
    ![alt text](Images/image-78.png)
    For icons we can use react-native-vector-icons library
    ![Docs](https://oblador.github.io/react-native-vector-icons/)
