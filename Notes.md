# React Native

- Fundamental Concepts

  - View Component
    - Text Component
    - Image Component
      ![Image](image.png)
    - Button Component
      ![Button](image-1.png)
    - TouchableOpacity Component
      ![TouchableOpacity](image-2.png)
      ![OnPress](image-3.png)
      ![TouchableHighlight](image-4.png)
    - Pressable Component
      ![Pressable](image-5.png)
    - SafeAreaView Component
      ![SafeAreaView](image-6.png)

- Styling
  Same as CSS but uses camelCase
  ![Styling](image-7.png)
  Passing as an object
  ![PassingAsObject](image-8.png)
  - StyleSheet
    ![StyleSheet](image-9.png)
    ![StyleSheet2](image-10.png)
    ![StyleSheet3](image-11.png)
    ![alt text](image-12.png)
    ![alt text](image-13.png)
    ![alt text](image-14.png)
    Don't use javascript objects for styles because it creates a new object on every render
    Instead use StyleSheet.create
    It loads only once
    For dynamic css we can use inline styles
    like onPress we can change the background color,etc
    Both combination of StyleSheet and inline styles works
  - Theme-based styling
    ![Theme-based styling](image-15.png)
    ![Theme-based styling2](image-16.png)
  - Use percentage as units
    ![Percentage](image-17.png)
  - Flexbox
    Flex helps us to divide the space
    ![alt text](image-18.png)
    ![alt text](image-19.png)
    ![alt text](image-20.png)
    ![alt text](image-21.png)
    ![alt text](image-22.png)
  - Flex Direction
    ByDefault it is vertical
    ![alt text](image-23.png)
    ![alt text](image-24.png)
    ![alt text](image-25.png)
  - Align Items and Justify Content
    ![alt text](image-26.png)
    ![alt text](image-27.png)
    ![alt text](image-28.png)
    ![alt text](image-29.png)
    ![alt text](image-30.png)
  - Align Self
    ![alt text](image-31.png)
  - Wrapping
    ![alt text](image-32.png)
    ![alt text](image-33.png)
    ![alt text](image-34.png)
    ![alt text](image-35.png)
    When flexWrap is set to wrap the align items works on lines and doesn't work properly
    So to center the items we can use alignContent on the parent container
    ![alt text](image-36.png)
    ![alt text](image-37.png)
  - Flex Grow
    If you assign flexGrow: 1 to a component, it will take up all the available space in its container.
    ![alt text](image-38.png)
    Works similarly to flex: 1
  - Flex Shrink
    If you assign flexShrink: 1 to a component, it will shrink to fit within its container if there is not enough space.
  - Flex Basis
    If you assign flexBasis: 100 to a component, it will take up 100 pixels of space in its container.

- ScrollView
  To make the content scrollable
  ![ScrollView](image-39.png)
  Also styling is different for ScrollView
  ![ScrollView2](image-40.png)
  ![ScrollView3](image-41.png)
- FlatList
  For large lists of data
  More efficient than ScrollView
  ![FlatList](image-42.png)
  ![FlatList2](image-43.png)
  Styling
  ![FlatList3](image-44.png)
  Props
  ![FlatList4](image-45.png)
  ![ColumnWrapperStyle](image-46.png)
  FlatList benefit over ScrollView is it only renders the items that are visible on the screen
  So it is more efficient for large lists of data
  extraData is used to re-render the list when the data changes
  ![extraData](image-47.png)
  ![horizontal](image-48.png)

- Handling User Input
  - TextInput
  ![TextInput](image-49.png)
  ![TextInput2](image-50.png)
  ![TextInput3](image-51.png)
  ![WholeCode](image-52.png)
  New Way to write onChangeText
  ![NewOnChangeText](image-52.png)
  - Properties
  ![TextInputProperties](image-53.png)
  More Properties
  [Documentation](https://reactnative.dev/docs/textInput)
  ![TextInput4](image-54.png)
  - Keyboard Types
  ![KeyboardTypes](image-55.png)
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
  ![Stack Navigation](image-56.png)
  ![Stack Navigation](image-57.png)
  ![alt text](image-58.png)
  ![alt text](image-59.png)
  ![alt text](image-60.png)
  ![alt text](image-61.png)
  ![alt text](image-62.png)
  - Props
   ![alt text](image-63.png)
   ![alt text](image-64.png)
  Top page will have no back button and will render first
  ![alt text](image-65.png)
  Also one property to set initialRouteName
  ![alt text](image-66.png)
  More properties
  ![alt text](image-67.png)
  [More Options](https://reactnavigation.org/docs/native-stack-navigator/#options)
  ![alt text](image-68.png)
  You can apply one option globally to all screens in the navigator with the screenOptions prop on the Stack.Navigator
  ![alt text](image-69.png)
  Global options can be overridden on a per-screen basis by specifying options on the individual screen.
  Stack Navigation helpers like navigation.navigate, navigation.push, navigation.pop, navigation.popToTop, navigation.replace, navigation.reset
  [Docs](https://reactnavigation.org/docs/native-stack-navigator/#helpers)
  
- Gemini Response:
Here is a brief, consolidated summary of the differences between **FlatList vs. map** and the key props for **FlatList** and **React Navigation**:

## 1. FlatList vs. `map()`

| Feature | `FlatList` | `Array.prototype.map()` |
| :--- | :--- | :--- |
| **Type** | Specialized **React Native Component** (with built-in scrolling). | **General JavaScript method**. |
| **Performance** | **High-Performance.** Uses **Virtualization** (lazy loading) to only render visible items, making it essential for **large/long lists** (e.g., feeds). | **Low-Performance.** Renders **all** items at once, causing lag/memory issues for large lists. |
| **Features** | Includes props for: Separators, Header/Footer, Pull-to-Refresh (`onRefresh`), and Infinite Scroll (`onEndReached`). | None. Requires manual implementation with `ScrollView`. |

---

## 2. Essential FlatList Props

These are the required or primary properties to make a list work:

| Prop | Category | Purpose |
| :--- | :--- | :--- |
| **`data`** | **Required** | The array of items to be displayed in the list. |
| **`renderItem`** | **Required** | A function that receives an individual list item (the `{ item }` object) and returns the component to render for it. |
| **`keyExtractor`** | **Essential** | A function to retrieve a unique string key for each item, which is vital for React's efficient rendering and updates. |
| **`numColumns`** | **Optional** | Renders items in a grid layout with the specified number of columns. |

### The `columnWrapperStyle` Prop

* **Function:** An optional style prop used to style the **internal container** (the "row wrapper") that holds the items when `numColumns` is greater than 1.
* **Purpose:** Primarily used to control spacing *between* columns (e.g., using `justifyContent: 'space-between'` or `gap`).
* **Limitation:** It is **ignored** if `numColumns` is `1` (the default).

---

## 3. React Navigation Props

These two props are automatically passed to **every screen component** defined in a Stack Navigator and have distinct roles:

| Prop | Role | Usage (The Action) | Data Access (The State) |
| :--- | :--- | :--- | :--- |
| **`navigation`** | **Controller/Actions** (The "How") | Use functions to move between screens: `navigation.navigate()`, `navigation.goBack()`, `navigation.push()`, `navigation.setOptions()`. | None. Used to *perform* navigation. |
| **`route`** | **Information/State** (The "What") | Read the current screen's metadata. | **`route.params`**: Accesses the data/parameters passed from the previous screen (e.g., `route.params.itemId`). |

  