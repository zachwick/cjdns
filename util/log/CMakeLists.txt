# You may redistribute this program and/or modify it under the terms of
# the GNU General Public License as published by the Free Software Foundation,
# either version 3 of the License, or (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.

add_library(cjdns-util-log
    Log.c
)

add_library(cjdns-util-log-writer
    WriterLog.c
)
target_link_libraries(cjdns-util-log-writer
    cjdns-util-log
)

add_library(cjdns-util-log-filewriter
    FileWriterLog.c
)
target_link_libraries(cjdns-util-log-filewriter
    cjdns-util-log-writer
    cjdio
)

add_library(cjdns-util-log-indirect
    IndirectLog.c
)
target_link_libraries(cjdns-util-log-indirect
    cjdns-util-log
)
