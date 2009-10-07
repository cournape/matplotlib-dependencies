from os.path import \
	join as pjoin

env = DefaultEnvironment(TARGET_ARCH="x86_64")
config = env.Configure()
assert config.CheckTypeSize("int*") == 8
config.Finish()

env.Append(CFLAGS=["/MD", "/O1"])

env["prefix"] = "#install"
env["includedir"] = pjoin(env["prefix"], "include")
env["libdir"] = pjoin(env["prefix"], "lib")
env["bindir"] = pjoin(env["prefix"], "bin")

env.Prepend(LIBPATH=[env["libdir"]])
env.Prepend(CPPPATH=[env["includedir"]])

SConscript("zlib123/SConscript", exports="env")
SConscript("lpng1240/SConscript", exports="env")
SConscript("freetype-2.3.9/SConscript", exports="env")
