MM=/home/dek/mm/micromanager/trunk
MMINSTALL=/usr/local
IMJ=/home/dek/ImageJ
CXXFLAGS=-c -fPIC -DPACKAGE_NAME=\"Micro-Manager\" -DPACKAGE_TARNAME=\"micro-manager\" -DPACKAGE_VERSION=\"1.4\" "-DPACKAGE_STRING=\"Micro-Manager 1.4\"" -DPACKAGE_BUGREPORT=\"info@micro-manager.org\" -DPACKAGE_URL=\"\" -DPACKAGE=\"micro-manager\" -DVERSION=\"1.4\" -DSTDC_HEADERS=1 -DHAVE_SYS_TYPES_H=1 -DHAVE_SYS_STAT_H=1 -DHAVE_STDLIB_H=1 -DHAVE_STRING_H=1 -DHAVE_MEMORY_H=1 -DHAVE_STRINGS_H=1 -DHAVE_INTTYPES_H=1 -DHAVE_STDINT_H=1 -DHAVE_UNISTD_H=1 -DHAVE_DLFCN_H=1 -DLT_OBJDIR=\".libs/\" "-DHAVE_BOOST=/**/" "-DHAVE_BOOST_THREAD=/**/" "-DHAVE_BOOST_ASIO=/**/" "-DHAVE_BOOST_SYSTEM=/**/" "-DHAVE_BOOST_CHRONO=/**/" "-DHAVE_BOOST_DATE_TIME=/**/" -DHAVE__BOOL=1 -DHAVE_STDBOOL_H=1 -DSTDC_HEADERS=1 -DHAVE_MEMSET=1 -I. -I$(MM) -pthread -I/usr/include -g -O0 -std=c++11

install: libmmgr_dal_ArduinoNeoPixel.so.0
	cp libmmgr_dal_ArduinoNeoPixel.so.0 $(IMJ)

libmmgr_dal_ArduinoNeoPixel.so.0: ArduinoNeoPixelShutter.o
	$(CXX)  -fPIC -DPIC -shared -o $@  $^ -L$(MM)/MMDevice/.libs -lMMDevice

ArduinoNeoPixelShutter.o: ArduinoNeoPixelShutter.cpp ArduinoNeoPixelShutter.h

clean:
	rm -f *.o *.so.0 *~
