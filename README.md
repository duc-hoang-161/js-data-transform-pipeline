# 🔄 JS Data Transform Pipeline

An interactive web application for visualizing and transforming JSON data using custom JavaScript code. Perfect for learning, prototyping, and understanding how array methods like `.map()`, `.filter()`, and `.reduce()` work!

## 🌟 Features

- **📥 Input JSON Data**: Paste or type JSON arrays directly into the input textarea
- **⚙️ Multiple Transformations**: Create unlimited transformation steps in a visual pipeline
- **🎯 Array Methods**: Support for:
  - `map` - Transform each element
  - `filter` - Select elements based on conditions
  - `reduce` - Aggregate data into a single value
  - `forEach` - Perform side effects
  - `flatMap` - Map and flatten arrays
  - `custom` - Write custom transformation logic with full array access
- **⚡ Live Mode**: Toggle real-time preview that updates as you type
- **📋 Copy to Clipboard**: One-click copy formatted output
- **🎨 Formatted Output**: Beautiful JSON formatting for readability
- **❌ Error Handling**: Clear error messages with step identification
- **📚 Quick Examples**: Pre-loaded examples to get started quickly
- **📱 Responsive Design**: Works on desktop and mobile devices
- **🎨 Modern UI**: Clean, intuitive interface with smooth animations

## 🚀 Getting Started

### Option 1: Open Directly
Simply open `index.html` in your web browser - no server required!

### Option 2: Use a Local Server
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (install http-server first)
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000` in your browser.

## 📖 How to Use

1. **Input Data**: Enter a JSON array in the input textarea
   ```json
   [
     {"name": "Alice", "age": 25},
     {"name": "Bob", "age": 30}
   ]
   ```

2. **Add Transformations**: Click "➕ Add Transformation" to create transformation steps

3. **Write Code**: In each transformation block:
   - Select the operation type (map, filter, reduce, etc.)
   - Write JavaScript code in the code editor
   - Use the provided parameters (item, index, array, etc.)

4. **Execute**: Click "▶️ Execute" or enable "Live Mode" for real-time updates

5. **View Output**: See the formatted result in the output textarea

6. **Copy Results**: Click "📋 Copy" to copy the output to clipboard

## 💡 Examples

### Example 1: Simple Map
Transform objects by adding a new field:
```javascript
// Input
[{"name": "Alice", "age": 25}, {"name": "Bob", "age": 30}]

// Transformation (map)
return { ...item, isAdult: item.age >= 18 };

// Output
[
  {"name": "Alice", "age": 25, "isAdult": true},
  {"name": "Bob", "age": 30, "isAdult": true}
]
```

### Example 2: Filter and Map Chain
Filter adults and then select specific fields:
```javascript
// Step 1 (filter)
return item.age >= 18;

// Step 2 (map)
return { name: item.name, city: item.city };
```

### Example 3: Reduce for Sum
Calculate total from array of objects:
```javascript
// Transformation (reduce)
return acc + (item.price * item.quantity);
```

## 🎯 Transformation Types

| Type | Parameters | Description | Return Value |
|------|-----------|-------------|--------------|
| **map** | `(item, index, array)` | Transform each element | New element |
| **filter** | `(item, index, array)` | Test each element | `true` to keep, `false` to remove |
| **reduce** | `(acc, item, index, array)` | Aggregate values | Accumulator |
| **forEach** | `(item, index, array)` | Side effects only | Nothing (void) |
| **flatMap** | `(item, index, array)` | Map and flatten | Array of elements |
| **custom** | `(data)` | Full control | Transformed data |

## 🛠️ Technical Details

- **Pure Client-Side**: No server required, all processing happens in the browser
- **Modern JavaScript**: Uses ES6+ features
- **No Dependencies**: Vanilla HTML, CSS, and JavaScript
- **Safe Execution**: Uses Function constructor for code execution
- **Error Boundaries**: Each transformation step has isolated error handling

## 🔒 Security Note

This tool uses JavaScript's `Function` constructor to execute user-provided code. While safe for local use and learning, **do not use this application with untrusted input** in a production environment without proper sandboxing.

## 🤝 Contributing

Contributions are welcome! Feel free to submit issues or pull requests.

## 📄 License

MIT License - feel free to use this project for learning and development!

## 🎓 Perfect For

- Learning JavaScript array methods
- Prototyping data transformations
- Teaching programming concepts
- Quick data manipulation tasks
- Understanding functional programming

---

Made with ❤️ for developers who love clean, visual tools!