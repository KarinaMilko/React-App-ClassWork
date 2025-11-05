# 🚀 Educational Project: React Core Concepts

This repository serves as a comprehensive collection of practical examples for learning the key concepts of the React library. Each component demonstrates a distinct aspect of development: from **basic state management** to **complex component lifecycle**, forms, validation, and working with global context.

## 🛠️ Technologies and Libraries Used

* **React** (Functional and Class Components, Hooks)
* **JavaScript** (ES6+)
* **CSS Modules / Sass Modules** (Local Styling)
* **Formik** & **Yup** (Form Creation and Validation)
* **Fetch API** (Data Fetching)
* **date-fns** (Date and Time Management)
* **classnames** (Conditional Class Joining)
* **prop-types** (Prop Type Checking)
* **react-icons** (UI Icons)

---

## 🏗️ Project Structure and Core Concepts

### **1. State Management and Component Lifecycle**

| Component | Concept | Demonstration |
| :--- | :--- | :--- |
| **`Counter`** | **`useState` (Functional)** | Basic usage of the **`useState`** hook and using a callback for safe state updates based on the previous value (`setCount(prevCount => ...)`). |
| **`CounterC`** | **Class Component** | Implementation of the same functionality using a **Class Component** (`this.state`, `this.setState()`, `this.props`). |
| **`StopWatch`** | **`useEffect` (Side Effects)** | Stopwatch implementation. Uses **`useEffect`** for interval management and **cleanup function** (`return () => clearInterval(id);`) to prevent **memory leaks**. Uses **`date-fns`** for time formatting.  |
| **`ViewPortParams`** | **`useEffect` (Events)** | Demonstrates working with **global DOM events** (`window.resize`). `useEffect` is used for event subscription and cleanup (`removeEventListener`). |
| **`UsersLoader`** | **Class Lifecycle, API, Local Storage** | A complex class component using lifecycle methods: **`componentDidMount`**, **`componentDidUpdate`**, and **`componentWillUnmount`**. Handles **API** calls and **`localStorage`** state persistence. |
| **`NavLinks`** | **Lifting State Up** | The parent component stores the active link state and passes the state change function (`changeActiveLink`) to child components, illustrating the **Lifting State Up** pattern. |

---

### **2. 🌐 Global State: Context API**

These components showcase how the **Context API** is used to manage the global application state (Theme, User) effectively, avoiding "prop drilling." 

| Component | Context Used | Purpose |
| :--- | :--- | :--- |
| **`UserHeader`** | `ThemeContext`, `UserContext` | Uses the **`useContext`** hook to **read** the user's name and current theme, and allows **changing** the global theme state. |
| **`UserFooter`** | `UserContext` | Demonstrates how deeply nested components can directly access user data without prop dependency. |

---

### **3. 📝 Forms and Validation**

| Component | Concept | Demonstration |
| :--- | :--- | :--- |
| **`LoginForm`** | **Controlled Inputs & RegExp** | A basic controlled form using **`useState`**. Utilizes **regular expressions** for initial client-side validation and conditional disabling of the submit button. |
| **`UserForm`, `ContactsForm`** | **Formik & Yup** | Advanced form handling using the **`Formik`** library for state management and **`Yup`** for defining complex validation schemas. |
| **`forms/Input`** | **Custom Input (Render Props)** | Creation of a **reusable input field** component that integrates with `Formik` via the **Render Props** pattern (`<Field>`). Dynamically displays error messages and styles the input based on validation status. |

---

### **4. Styling and UI Patterns**

| Component | Concept | Demonstration |
| :--- | :--- | :--- |
| **`CategoriesList`** | **Dynamic Styling** | Renders a list from an array. Uses the **`classnames`** library for conditionally applying CSS classes based on data values. |
| **`Header`** | **Conditional Rendering** | Uses the `isLogin` prop to conditionally display either a user avatar or the `LogIn`/`SignUp` buttons. |
| **`ImageWrapper`** | **`children` Prop & `prop-types`** | Demonstrates the **`children`** pattern (a wrapper container) and uses **`prop-types`** for explicit checking of expected prop types. |
| **`Weather`** | **API Fetch & UI Icons** | Fetches weather data from the **Open-Meteo API** and displays it. Uses **`react-icons`** for visual representation. |

---

## 💡 Project Setup

To run the project locally:

```bash
# 1. Clone the repository
git clone <YOUR_REPOSITORY_URL>

# 2. Navigate to the project folder
cd <project_folder_name>

# 3. Install dependencies
npm install

# 4. Start the project in development mode
npm run dev
