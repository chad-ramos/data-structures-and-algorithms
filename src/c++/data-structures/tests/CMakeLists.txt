﻿cmake_minimum_required (VERSION 3.8)

set(This DataStructuresTests)

set(Sources
	"dynamic-array-tests.cpp"
	"doubly-linked-list.cpp"
)

add_executable (${This} ${Sources})

target_link_libraries(${This} PUBLIC
	gtest_main
	DataStructures
)

add_test(
	NAME ${This}
	COMMAND ${This}
)