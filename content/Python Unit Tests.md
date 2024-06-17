Testing small snippets of code (may not be necessarily exposed to the user) to make sure they work

Using PyUnit (``import unittest``)
- Subclass ``unittest.TestCase`` 

``self.assertEqual(x, y, msg=None)``
If the test fails, ``msg`` will be printed