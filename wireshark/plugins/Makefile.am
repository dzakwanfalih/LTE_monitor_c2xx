# Makefile.am
# Automake file for Wireshark plugins
#
# $Id: Makefile.am 47992 2013-03-01 23:53:11Z rbalint $
#
# Wireshark - Network traffic analyzer
# By Gerald Combs <gerald@wireshark.org>
# Copyright 1998 Gerald Combs
#
# This program is free software; you can redistribute it and/or
# modify it under the terms of the GNU General Public License
# as published by the Free Software Foundation; either version 2
# of the License, or (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

-include Custom.make

SUBDIRS = $(_CUSTOM_SUBDIRS_) \
	asn1 \
	docsis \
	ethercat \
	gryphon \
	irda \
	m2m \
	mate \
	opcua \
	profinet \
	stats_tree \
	unistim \
	wimax \
	wimaxasncp \
	wimaxmacphy

plugindir = @plugindir@

EXTRA_DIST = \
	$(_CUSTOM_EXTRA_DIST_) \
	plugins.vcproj \
	Makefile.common.inc \
	Makefile.nmake \
	Custom.make.example \
	Custom.m4.example \
	Custom.nmake.example

MAINTAINERCLEANFILES = \
	Makefile.in

checkapi:
	for i in $(SUBDIRS); do \
		(cd "$$i"; $(MAKE) checkapi); \
	done

