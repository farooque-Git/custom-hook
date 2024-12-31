# Custom Hook

A simple and reusable custom hook for managing form state in React. This hook helps you manage form data, handle input changes, and reset the form with ease.

## Installation

You can install the package via npm or yarn:

### Using npm:
```bash
npm install hocrux

Using yarn:
bash
Copy code
yarn add hocrux
Usage
Here’s how to use the useForm hook in your React project:

1. Import the hook:
tsx
Copy code
import { useForm } from 'hocrux';
2. Use the hook in your component:
tsx
Copy code
import React from 'react';
import { useForm } from 'hocrux';

const MyForm = () => {
  const [formData, handleChange, resetForm] = useForm({
    username: '',
    email: '',
  });

  const handleSubmit = (event: React.FormEvent) => {
    event.preventDefault();
    console.log(formData);
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        name="username"
        value={formData.username}
        onChange={handleChange}
      />
      <input
        type="email"
        name="email"
        value={formData.email}
        onChange={handleChange}
      />
      <button type="submit">Submit</button>
      <button type="button" onClick={resetForm}>Reset</button>
    </form>
  );
};
3. Explanation:
useForm returns:

formData: The current form data.
handleChange: A function to update the form data when an input changes.
resetForm: A function to reset the form to its initial values.
API
useForm(initialValues: object)
initialValues: An object containing the initial values for the form fields.
Returns an array with three elements:

formData: The current state of the form.
handleChange: A function to update the form state when an input changes.
resetForm: A function to reset the form to its initial values.
License
MIT © [Your Name]

vbnet
Copy code

### Key Improvements:
1. **Formatting**: Fixed code blocks and made sure the syntax for markdown, JavaScript, and TypeScript is correct.
2. **Clarity**: Added more explanatory text to the "Usage" and "API" sections to help users understand how to implement the hook.
3. **License**: The `MIT` license section is now properly formatted. Replace `[Your Name]` with your actual name for copyright purposes.

### Next Steps:
- **Customization**: Make sure to update the **license** section with your name and check if any other details in the package need adjusting.
- **Testing**: Ensure your README provides all the necessary info users need to get started with your package.

Let me know if you'd like further adjustments!
