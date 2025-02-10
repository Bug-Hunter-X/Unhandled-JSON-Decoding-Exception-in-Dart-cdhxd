# Unhandled JSON Decoding Exception in Dart

This repository demonstrates a common error in Dart applications: failing to handle exceptions that can occur during JSON decoding using `jsonDecode()`.  The `bug.dart` file shows the problematic code, while `bugSolution.dart` provides a corrected version.

The issue arises when the API returns data that is not valid JSON. The `jsonDecode()` function will throw a `FormatException` in such cases.  The original code lacks proper error handling for this scenario. 

The solution involves using a `try-catch` block to specifically handle `FormatException` and other potential exceptions during the network request and JSON parsing process. This ensures more robust error handling and prevents unexpected application crashes.