troykinsella.java
=================

An ansible role for installing the Oracle Java SE Development Kit. Default version: 8u92.

Dependencies
------------

* troykinsella.archive

Role Variables
--------------

* java_version: Optional. The version of java to install. Default: 8u92.
* java_minor_version: Optional. The minor java version used in the archive path. Default: b14.
* java_archive_os: Optional. The target operating system. Default: linux.
* java_archive_architecture: Optional. The target system architecture. Default: x64.
* java_archive_base_url: Optional. The installation archive base URL. Default: http://download.oracle.com/otn-pub/java/jdk/{{ java_version }}-{{ java_minor_version }}/{{ java_archive_filename }}.
* java_archive_checksum: Optional. The expected installation archive checksum. Default: 79a3f25e9b466cb9e969d1772ea38550de320c88e9119bf8aa11ce8547c39987.
* java_archive_checksum_algorithm: Optional. The installation archive checksum algorithm. Default: sha256.
* java_archive_cache_path: Optional. The directory path into which the archive will be downloaded. Default: /usr/local/pkg.
* java_archive_destination_path: Optional. The installation prefix directory path. Default: /usr/local.
* java_archive_extracted_file_name: Optional. The expected name of the root file or directory that is extracted from the archive. Default: jdk1.8.0_92.
* java_archive_destination_file_name: Optional. Rename the extracted directory to this value.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: troykinsella.java

License
-------

MIT
