cmake_minimum_required(VERSION 3.0)
project(test)
find_package(absl REQUIRED )
find_package(Protobuf REQUIRED )

add_executable(test main.cc test.pb.cc)
target_link_libraries(
        ${Protobuf_LIBRARIES}
        absl::log_internal_message
        absl::log_internal_check_op
)
