## Integration of a Mathematical Calulations with a Chat Completion System using LLM Function-Calling

# AIM:
To design and implement a Python function for calculating the area of a rectangle ,  
integrate it with a chat completion system utilizing the function-calling feature of a large language model (LLM).

## PROBLEM STATEMENT:
Design and implement a system where a user can input dimensions of a rectangle (length and width),  
and the system calculates its area by invoking a Python function using the function-calling capabilities of an LLM.


## DESIGN STEPS:

1. Import necessary libraries, including OpenAI for LLM integration and math for mathematical operations.
2. Define a Python function to calculate the area of a rectangle  based on its length and width.
3. Integrate the function into an LLM-based chat completion system with function-calling capabilities.



## PROGRAM:

```
import openai

# Define the function to calculate the area of a rectangle
def calculate_rectangle_area(length, width):
    return length * width

# Example function to simulate OpenAI's function-calling integration
def mock_llm_function_call(function_name, arguments):
    if function_name == "calculate_rectangle_area":
        return {"area": calculate_rectangle_area(**arguments)}
    else:
        return {"error": "Function not recognized"}

# Simulate user interaction and LLM response
def main():
    user_message = "What is the area of a rectangle with length 8 and width 5?"
    print(f"User: {user_message}")
    
    # Simulated LLM recognizing the intent and invoking the function
    function_name = "calculate_rectangle_area"
    arguments = {"length": 8, "width": 5}
    
    # Mocking LLM function calling response
    response = mock_llm_function_call(function_name, arguments)
    print(f"LLM Function Output: {response}")

    # Returning output to user
    if "area" in response:
        print(f"Bot: The area of the rectangle is {response['area']} square units.")
    else:
        print("Bot: Sorry, there was an error processing your request.")

# Execute the main function
if __name__ == "__main__":
    main()

```
## OUTPUT:
![Screenshot 2024-11-24 123159](https://github.com/user-attachments/assets/4d326487-a146-4c48-a220-53db069e4ed4)


## RESULT:
Hence,the python program to design and implement a Python function for calculating the area of a rectangle ,  
integrating it with a chat completion system utilizing the function-calling feature of a large language model (LLM) is written successfully and executed.
