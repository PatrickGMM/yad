AM_CPPFLAGS = -DLOCALEDIR=\""$(datadir)/locale"\"

bin_PROGRAMS = yad

yad_SOURCES = 		\
	about.c			\
	app.c			\
	calendar.c		\
	color.c			\
	dnd.c           \
	entry.c			\
	file.c			\
	font.c			\
	form.c			\
	icons.c			\
	list.c			\
	notebook.c		\
	option.c		\
	paned.c			\
	picture.c       \
	print.c			\
	progress.c		\
	scale.c			\
	text.c			\
	util.c			\
	main.c			\
	yad.h			\
	calendar.xpm

if TRAY
yad_SOURCES += notification.c
endif

if HTML
yad_SOURCES += html.c
endif

yad_CFLAGS = $(GTK_CFLAGS) $(HTML_CFLAGS) $(SPELL_CFLAGS) $(SOURCEVIEW_CFLAGS)
yad_LDADD = $(GTK_LIBS) $(HTML_LIBS) $(SPELL_LIBS) $(SOURCEVIEW_LIBS)

if BUILD_PFD
bin_PROGRAMS += pfd

pfd_SOURCES = pfd.c
pfd_CFLAGS = $(PFD_CFLAGS)
pfd_LDADD = $(PFD_LIBS)
endif

if BUILD_IB
bin_PROGRAMS += yad-icon-browser

yad_icon_browser_SOURCES = browser.c
yad_icon_browser_CFLAGS = $(GTK_CFLAGS)
yad_icon_browser_LDADD = $(GTK_LIBS)
endif
