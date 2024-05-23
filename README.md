def celsius_to_fahrenheit(celsius): return (celsius * 9/5) + 32

def celsius_to_kelvin(celsius): return celsius + 273.15

def fahrenheit_to_celsius(fahrenheit): return (fahrenheit - 32) * 5/9

def fahrenheit_to_kelvin(fahrenheit): return (fahrenheit + 459.67) * 5/9

def kelvin_to_celsius(kelvin): return kelvin - 273.15

def kelvin_to_fahrenheit(kelvin): return (kelvin * 9/5) - 459.67

def convert_temperature(value, unit): if unit.lower() == 'c': fahrenheit = celsius_to_fahrenheit(value) kelvin = celsius_to_kelvin(value) return f"{value}°C is {fahrenheit:.2f}°F and {kelvin:.2f}K" elif unit.lower() == 'f': celsius = fahrenheit_to_celsius(value) kelvin = fahrenheit_to_kelvin(value) return f"{value}°F is {celsius:.2f}°C and {kelvin:.2f}K" elif unit.lower() == 'k': celsius = kelvin_to_celsius(value) fahrenheit = kelvin_to_fahrenheit(value) return f"{value}K is {celsius:.2f}°C and {fahrenheit:.2f}°F" else: return "Invalid unit of measurement."

def main(): try: value = float(input("Enter the temperature value: ")) unit = input("Enter the unit of measurement (C for Celsius, F for Fahrenheit, K for Kelvin): ") result = convert_temperature(value, unit) print(result) except ValueError: print("Invalid input. Please enter a numerical temperature value.")

if name == "main": main()
