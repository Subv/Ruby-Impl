# Copyright (C) 2008-2011 TrinityCore <http://www.trinitycore.org/>
#
# This file is free software; as a special exception the author gives
# unlimited permission to copy and/or distribute it, with or without
# modifications, as long as this notice is preserved.
#
# This program is distributed in the hope that it will be useful, but
# WITHOUT ANY WARRANTY, to the extent permitted by law; without even the
# implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

# NOTE: Do not use glob here, it would include files we don't want
file(GLOB_RECURSE sources_Accounts Accounts/*.cpp Accounts/*.h)

set(ruby_STAT_SRCS
  ${sources_Accounts}

add_library(ruby SHARED ${ruby_STAT_SRCS})

install(TARGETS ruby RUNTIME DESTINATION "${CMAKE_INSTALL_PREFIX}")
