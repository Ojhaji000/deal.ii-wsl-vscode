cmake_minimum_required(VERSION 3.13.4)
project(step1 LANGUAGES CXX)

find_package(deal.II 9.6.0 REQUIRED
  HINTS /usr/share/cmake/deal.II $ENV{DEAL_II_DIR}
)

deal_ii_initialize_cached_variables()

# ✅ Define the executable first
add_executable(step1 step1.cc)

# ✅ Then apply deal.II macros to it
deal_ii_setup_target(step1)

