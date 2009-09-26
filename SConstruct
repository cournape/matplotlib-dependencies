from os.path import \
	join as pjoin

tools = ["msvs", "msvc", "mslink", "mslib"]
env = DefaultEnvironment(tools=tools)

env.Append(CFLAGS=["/MD", "/W3", "/Ox"])

env["prefix"] = "#install"
env["includedir"] = pjoin(env["prefix"], "include")
env["libdir"] = pjoin(env["prefix"], "lib")
env["bindir"] = pjoin(env["prefix"], "bin")

env.Prepend(LIBPATH=[env["libdir"]])
env.Prepend(CPPPATH=[env["includedir"]])

SConscript("zlib123/SConscript", exports="env")
SConscript("lpng1240/SConscript", exports="env")
