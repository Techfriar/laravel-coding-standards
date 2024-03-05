[<<Back](../README.md)

## Exceptions Handling:

    ```php
    try {
    $user = User::findOrFail($userId);
    } catch (ModelNotFoundException $e) {
    // Handle the case where the user is not found
    return response()->json(['error' => 'User not found'], 404);
    }
    ```
    
## Validation Errors  : 

    ```php
    class StoreUserRequest extends FormRequest
    {
        public function authorize()
        {
            return true;
        }

        public function rules()
        {
            return [
                'name' => 'required',
                'email' => 'required|email',
            ];
        }

        public function messages()
        {
            return [
                'name.required' => 'Name is required.',
                'email.required' => 'Email is required.',
                'email.email' => 'Invalid email format.',
            ];
        }
    }
    ```

## API Error Handling :

    ```php
    public function updateUser(Request $request, $id)
    {
        $user = User::find($id);

        if (!$user) {
            return response()->json(['error' => 'User not found'], 404);
        }

        // Update user logic here

        return response()->json(['message' => 'User updated successfully'], 200);
    }
    ```



    ```php
    if ($user) {
        // Return response
        return $this->formatResponse([
            'status' => true,
            'message' => 'Profile updated successfully',
        ],200),;
    } else {
        return $this->formatResponse([
            'status' => false,
            'message' => 'Failed to update users details'
        ], 422);
    }
    ```
