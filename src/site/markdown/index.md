# Overview

This test engine is designed to test implementations of the Web Feature
Service 1.0.0 with filters defined using OGC Filter Encoding 1.0.0
specification and features defined using Geography Markup Language 2.1.2
specification.

This test suite is based on the following documents:

  * _Web Feature Service Implementation Specification_, version 1.0.0 [OGC 02-058] ([PDF version](http://portal.opengeospatial.org/files/index.php?artifact_id=7176), [HTML version](OGCTestData/wfs/1.0.0/specs/wfs/1.0.0/02-058.html))
  * _Filter Encoding Implementation Specification_, version 1.0.0 [OGC 02-059] ([PDF version](http://portal.opengeospatial.org/files/?artifact_id=1171), [HTML version](OGCTestData/wfs/1.0.0/specs/filter/1.0.0/02-059.html))
  * _Web Feature Service Requirements_ ([HTML version](testreq.html))
  * _Test Data for WFS 1.0.0 tests_ ([Test Data](http://cite.opengeospatial.org/teamengine/about/wfs/1.0.0/web/data/data-wfs-1.0.0.zip))

# Description

The [Executive Summary](execsummary.html) provides an overview description of
the test.

The assertions implemented in this test can be found in the document
summarizing the [requirements](testreq.html).

The Web Feature service defines the following profiles of implementations. An
implementation will be tested for compliance with one of these profiles based
on the operations supported in the capabilities document.

  * **Basic** \- GetCapabilities, DescribeFeatureType and GetFeature
  * **Transactional** \- Basic + Transaction
  * **Locking** \- Transactional + LockFeature and GetFeatureWithLock

# Release Notes

Release notes are available at the [relnotes.html](relnotes.html) page.
