# Makefile.am-- 
# Copyright 2004-2006, 2008,2011-13 Red Hat Inc., Durham, North Carolina.
# All Rights Reserved.
#
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307  USA
#
# Authors:
#   Steve Grubb <sgrubb@redhat.com>
#

CONFIG_CLEAN_FILES = *.rej *.orig
AUTOMAKE_OPTIONS = no-dependencies
INCLUDES = -I${top_srcdir} -I${top_srcdir}/lib -I${top_srcdir}/src/libev -I${top_srcdir}/auparse
sbin_PROGRAMS = auditctl
AM_CFLAGS = -D_GNU_SOURCE
noinst_HEADERS = auditd-config.h auditd-event.h auditd-listen.h ausearch-llist.h ausearch-options.h auditctl-llist.h aureport-options.h ausearch-parse.h aureport-scan.h ausearch-lookup.h ausearch-int.h auditd-dispatch.h ausearch-string.h ausearch-nvpair.h ausearch-common.h ausearch-avc.h ausearch-time.h ausearch-lol.h 

auditctl_SOURCES = auditctl.c auditctl-llist.c delete_all.c
auditctl_CFLAGS = -fPIE -DPIE -g -D_GNU_SOURCE
auditctl_LDFLAGS = -pie -Wl,-z,relro -Wl,-z,now
auditctl_LDADD = -L${top_builddir}/lib -laudit
