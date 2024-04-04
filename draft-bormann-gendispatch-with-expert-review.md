---
title: Registry policies “… with Expert Review”
# abbrev: "TODO - Abbreviation"
category: bcp

docname: draft-bormann-gendispatch-with-expert-review-latest
submissiontype: IETF
updates: 7120, 8126
number:
date:
consensus: true
v: 3
area: General
workgroup: General Area Dispatch
keyword:
 - IANA
 - Designated Expert
venue:
  mail: gendispatch@ietf.org
  github: cabo/with-expert-review

author:
  - name: Carsten Bormann
    org: Universität Bremen TZI
    street: Postfach 330440
    city: Bremen
    code: D-28359
    country: Germany
    phone: +49-421-218-63921
    email: cabo@tzi.org
  - name: Marco Tiloca
    org: RISE AB
    street: Isafjordsgatan 22
    city: Kista
    code: SE-16440 Stockholm
    country: Sweden
    email: marco.tiloca@ri.se

normative:
  BCP100:
#   RFC7120:
  BCP26:
#   RFC8126:
  RFC8729: bodies

informative:


--- abstract

[^a1-]: This document updates
[^a1-] RFC 8126, [^a2-]

[^a2-]: adding registry policies that augment an existing policy that is based on a review body action with the additional requirement for a Designated Expert review.

[^a3-]: It also updates
[^a3-] RFC 7120 [^a4-]

[^a4-]: with the necessary process to perform early allocations for registries with one of the augmented policies.


--- middle

# Introduction

{{Section 4 of RFC8126@BCP26}} defines a number of _well-known policies_
that can be referenced as registration policies from documents that
set up IANA registries.
Some of these policies involve a _Designated Expert_, who is
intended to be aware of the fine points of what should or should not
become a registration in that registry ({{Sections 4.5 and 4.6 of RFC8126@BCP26}}).
Some other policies involve a _review body_ that autonomously, not
involving a _Designated Expert_, decide whether a registration should
be accepted ({{Sections 4.7, 4.8, 4.9, and 4.10 of RFC8126@BCP26}}).

In the past, this has occasionally led to friction where a Designated
Expert was not consulted by the review body before approving the
registration, missing some finer point (such as certain consistency
requirements) that would have been pointed out by the expert.

[^a1-] {{Section 4 of RFC8126@BCP26}}, [^a2-]

[^a3-] {{Sections 2 and 3 of RFC7120@BCP100}} [^a4-]


# Augmented Registration Policies {#augment}

For each of the well-known policies defined in {{Sections 4.7, 4.8,
4.9, and 4.10 of RFC8126@BCP26}}, this document adds a parallel _augmented
policy_ that also specifies involving a Designated Expert.

## RFC Required With Expert Review {#rfcreq}

This policy is identical to a combination of {{Sections 4.6 and 4.7 of RFC8126@BCP26}}.
The RFC to be published serves as the documentation required by
{{Section 4.6 of RFC8126@BCP26}}.
It is the responsibility of the stream approving body (see {{Section
5.1 of RFC8729}}) to ensure that an approval for the registration by
the Designated Expert is obtained before approving the RFC
establishing the registration.

## IETF Review With Expert Review {#ietfrev}

This policy is identical to a combination of {{Sections 4.6 and 4.8 of RFC8126@BCP26}}.
The RFC to be published serves as the documentation required by
{{Section 4.6 of RFC8126@BCP26}}.
It is the responsibility of the IESG to ensure that an approval for
the registration by the Designated Expert is obtained before approving
the RFC establishing the registration.

## Standards Action With Expert Review {#stdsact}

This policy is identical to a combination of {{Sections 4.6 and 4.9 of
RFC8126@BCP26}}, mirroring the requirements of {{ietfrev}}
narrowed down to a certain type of RFC to be published.

## IESG Approval With Expert Review

This policy is identical to a combination of either
Section {{4.5<RFC8126}} or Section {{4.6<RFC8126}}
with {{Section 4.10 of RFC8126@BCP26}}, depending on the discretion of
the IESG mentioned in the first paragraph of the latter section (which
may be additionally informed by input from the Designated Expert).
It is the responsibility of the IESG to ensure that an approval for
the registration by the Designated Expert is obtained before approving
the registration.


# Early Allocation for Augmented Registration Policies

This document updates {{RFC7120@BCP100}} to apply to the augmented policies
defined above in {{rfcreq}}, {{ietfrev}}, and {{stdsact}}.

Specifically:

* Item (a) in {{Section 2 of RFC7120@BCP100}} is extended to include the
  three augmented policies.
* Item (2) in {{Section 3.1 of RFC7120@BCP100}} is amended as follows:

{:quote}
> {: start="2"}
  2. The WG chairs determine whether the conditions for early
     allocations described in Section 2 are met, particularly
     conditions (c) and (d).
     For the registration policies defined in {{augment}} of
     RFC-XXXX, the WG chairs first request review and approval from
     the Designated Expert.

[^XXXX]

[^XXXX]: RFC editor: please replace XXXX by the RFC number of this
    document and delete this note.

# Security Considerations

The security considerations of {{Section 5 of RFC7120@BCP100}} and
{{Section 12 of RFC8126@BCP26}} apply.
Augmenting registration policies by Designated Expert involvement may
help reduce the potential of introducing security issues by
adding inconsistent or insecure registrations to a registry.

# IANA Considerations

This document is all about procedures that need to be implemented by
IANA, but by itself has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

The creation of this document was prompted by an IESG ballot comment
from John Scudder, which led to the observation that the now somewhat
common practice of augmenting review-body-based registry policies by
Expert Review had not been documented sufficiently.
