# Discord GameSDK

# NOTE: discord-rpc is to be deprecated in place of Discord GameSDK.
# The rpcs3 codebase is to be migrated forthcoming.


if (USE_DISCORD_GAMESDK AND (CMAKE_SYSTEM MATCHES "Linux" OR MSVC OR APPLE))

    add_library(discord_game_sdk STATIC)

    file(GLOB_RECURSE discord_game_sdk_src "src/cpp/*.cpp")

    file(GLOB_RECURSE discord_game_sdk_headers "src/cpp/*.h")

    target_sources(discord_game_sdk 
    PUBLIC
    ${discord_game_sdk_src}
    )


endif()
