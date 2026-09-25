Triage.py Output:
```PS C:\Internship\task 2\2> python triage.py
    Email: I want to know the status of my coffee order.
    Result: {"category": "order", "confidence": 0.92}

    Email: Your coffee was excellent. I really enjoyed it.
    Result: {"category": "feedback", "confidence": 0.88}

    Email: My order arrived damaged. Please help.
    Result: {"category": "order", "confidence": 0.92}

    Email: I am not sure what category this email belongs to.
    Result: {"category": "Uncertain", "confidence": 0.45}
```
Test_traige.py output:

================= test session starts =================
platform win32 -- Python 3.12.10, pytest-9.1.1, pluggy-1.6.0 -- C:\Users\mrj82\AppData\Local\Programs\Python\Python312\python.exe
cachedir: .pytest_cache
rootdir: C:\Internship\task 2\2
plugins: anyio-4.15.1
collected 7 items                                                     

test_triage.py::test_normal_classification PASSED               [ 14%] 
test_triage.py::test_low_confidence_becomes_uncertain PASSED    [ 28%] 
test_triage.py::test_prompt_injection PASSED                    [ 42%] 
test_triage.py::test_empty_email PASSED                         [ 57%]
test_triage.py::test_whitespace_email PASSED                    [ 71%] 
test_triage.py::test_result_contains_required_keys PASSED       [ 85%] 
test_triage.py::test_confidence_range PASSED                    [100%] 

================= 7 passed in 0.09s ================== 