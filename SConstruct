env = Environment()
env.Append(CXXFLAGS='-O2 -g')
env.ParseConfig('pkg-config --cflags --libs gtk+-2.0')
conf= Configure(env)
if not conf.CheckLib('gtk'):
	print "Brak biblioteki GTK"
	Exit(1)
if not conf.CheckLib('SDL'):
	print "Brak SDLa"
	Exit(1)
env=conf.Finish()
env.Program(target="quickEdit", source=['main.cpp'])
