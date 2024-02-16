import unittest
from main.test_login import TestLogin
from main.test_logout import TestLogout
from main.test_status_check import TestStatusCheck
from main.test_send_payment import TestSendPayment
from main.test_receive_payment import TestReceivePayment
from main.test_authorization import TestAuthorization

# Define a TestSuite
test_suite = unittest.TestSuite()

# Add test cases from each test class
test_suite.addTest(unittest.makeSuite(TestLogin))
test_suite.addTest(unittest.makeSuite(TestLogout))
test_suite.addTest(unittest.makeSuite(TestStatusCheck))
test_suite.addTest(unittest.makeSuite(TestSendPayment))
test_suite.addTest(unittest.makeSuite(TestReceivePayment))
test_suite.addTest(unittest.makeSuite(TestAuthorization))

# Run the TestSuite
unittest.TextTestRunner().run(test_suite)
