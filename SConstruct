from os.path import \
	join as pjoin

tools = ["msvs", "msvc", "mslink", "mslib"]
env = DefaultEnvironment(tools=tools)

env.Append(CFLAGS=["/MD", "/W3", "/Ox"])
env["prefix"] = "#install"
env["includedir"] = pjoin(env["prefix"], "include")
env["libdir"] = pjoin(env["prefix"], "lib")

SConscript("zlib123/SConscript", exports="env")
