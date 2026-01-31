# add_repo(
#   example <- Name
#   https://github.com/example/example.git <- Link Repository
#   0.1 <- Version
# )

# Helper Function
include(FetchContent)

function(add_repo name repo tag)
  FetchContent_Declare(
    ${name}
    GIT_REPOSITORY ${repo}
    GIT_TAG ${tag}
  )
  FetchContent_MakeAvailable(${name})
endfunction()
