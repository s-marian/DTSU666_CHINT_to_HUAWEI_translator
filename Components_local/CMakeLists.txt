					
set(SRC_NEW
  PubSubClient.cpp
  )

set(srcs ${SRC_NEW} )

idf_component_register(SRCS ${srcs} INCLUDE_DIRS "./" )


