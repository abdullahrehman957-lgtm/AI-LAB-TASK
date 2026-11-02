def check_result(score, documents, attendance, verification):
 if score >= 70 and documents == True and attendance >= 75 and verification >= 60:
return "Pass"
else:
return "Fail"
test_cases = [
(85, True, 80, 75),
(85, True, 70, 75),
(85, True, 80, 55),
(70, True, 75, 60)
]
for i in range(4):
score = test_cases[i][0]
documents = test_cases[i][1]
attendance = test_cases[i][2]
verification = test_cases[i][3]
actual = check_result(score, documents, attendance, verification)
if i == 0:
expected = "Pass"
reason = "All conditions are satisfied."
elif i == 1:
expected = "Fail"
reason = "Attendance is below 75%."
elif i == 2:
expected = "Fail"
reason = "Verification score is below 60."
else:
expected = "Pass"
reason = "All values are at the threshold."
print("Test Case:", i + 1)
print("Input:", test_cases[i])
print("Expected Result:", expected)
print("Actual Result:", actual)
print("Reason:", reason)
print("----------------------")
