This is working demo of basic google protocol buffer usage. It writes and reads a address book.


To generate boiler-plate code, run:

> protoc -I=$SRC_DIR --cpp_out=$DST_DIR $SRC_DIR/addressbook.proto

You might come across a linker error.

Try adding PROTOBUF_USE_DLLS in preprocessor.

Note: Cross check the architecture whether it is x86 or x64. Make sure you are using proper lib and dll for debug and release versions.

You need to specify path of lib in Linker-->Additional dependencies.
Additionally, need to specify additional directory path also.

Also, need to copy libprotobuf.dll besides your final exe in 'Debug' or 'Release' folder. [Load time dll]
