## Integration of a Mathematical Calulations with a Chat Completion System using LLM Function-Calling

### AIM:
To design and implement a Python function for calculating the volume of a cylinder, integrate it with a chat completion system utilizing the function-calling feature of a large language model (LLM).

### PROBLEM STATEMENT:
Design and implement a system where a user can input dimensions of a cylinder (radius and height),
and the system calculates its volume by invoking a Python function using the function-calling capabilities of an LLM.

### DESIGN STEPS:
### STEP 1
import necessary libraries, including OpenAI for LLM integration and math for mathematical operations.
### STEP 2
Define a Python function to calculate the volume of a cylinder based on its radius and height.
### STEP 3
Integrate the function into an LLM-based chat completion system with function-calling capabilities.

### PROGRAM:
```
Name: Karthik padmanaban R
Reg no: 212224110029

import openai
import math

# Define the function to calculate the volume of a cylinder
def calculate_cylinder_volume(radius, height):
    return math.pi * radius ** 2 * height

# Example function to simulate OpenAI's function-calling integration
def mock_llm_function_call(function_name, arguments):
    if function_name == "calculate_cylinder_volume":
        return {"volume": calculate_cylinder_volume(**arguments)}
    else:
        return {"error": "Function not recognized"}

# Simulate user interaction and LLM response
def main():
    user_message = "What is the volume of a cylinder with radius 7 and height 15?"
    print(f"User: {user_message}")
    
    # Simulated LLM recognizing the intent and invoking the function
    function_name = "calculate_cylinder_volume"
    arguments = {"radius": 5, "height": 10}
    
    # Mocking LLM function calling response
    response = mock_llm_function_call(function_name, arguments)
    print(f"LLM Function Output: {response}")

    # Returning output to user
    if "volume" in response:
        print(f"Bot: The volume of the cylinder is {response['volume']:.2f}.")
    else:
        print("Bot: Sorry, there was an error processing your request.")

# Execute the main function
if __name__ == "__main__":
    main()
```

### OUTPUT:
<img width="771" height="84" alt="Screenshot 2025-09-19 114050" src="https://github.com/user-attachments/assets/44850b54-f3e4-4971-a859-cfae96850b84" />

### RESULT:
Hence,the python program to design and implement a Python function for calculating the volume of a cylinder,
integrating it with a chat completion system utilizing the function-calling feature of a large language model (LLM) is written successfully and executed.
