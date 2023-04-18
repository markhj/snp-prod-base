[
  id: react-provider-pattern
  tags:
  locations:
]: #

# Provider pattern

## Provider component

````jsx
import React, { createContext, useState } from 'react';

const MyContext = createContext();

export const useMyContext = () => {
  const context = React.useContext(MyContext);
  if (!context) {
    throw new Error('useMyContext must be used within a MyContextProvider');
  }
  return context;
};

export const MyContextProvider = ({ children }) => {
  const [value, setValue] = useState('');

  const updateValue = (newValue) => {
    setValue(newValue);
  };

  return (
    <MyContext.Provider value={{ value, updateValue }}>
      {children}
    </MyContext.Provider>
  );
};
````

## Wrap

````jsx
import { MyContextProvider } from './MyContext';

// ...

return
  <MyContextProvider>
    {/* Child components */}
  </MyContextProvider>
````


## Usage

````jsx
import { useMyContext } from './MyContext';

const ChildComponent = () => {
  const { value, updateValue } = useMyContext();

  const handleChange = (event) => {
    updateValue(event.target.value);
  };

  return (
    <div>
      <input type="text" value={value} onChange={handleChange} />
      <p>Value: {value}</p>
    </div>
  );
};
````
