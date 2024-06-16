Error trigger - Left 2D scan process, and the error fired when the laptop entered its sleep state (I was afk)

Trace:

1.) ConsoleHelper.cpp - `DppLibUsb.SendPacketUSB(DppLibUsb.DppLibusbHandle, DP5Proto.BufferOUT, DP5Proto.PacketIn);`
2.) DppLibUsb.cpp - `int CDppLibUsb::SendPacketUSB(...)`
	``result <= 0`` 