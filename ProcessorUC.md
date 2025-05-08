# © Intel Corporation. All Rights Reserved. 

# Processor Use Condition Data

**SMBIOS** (System Management BIOS) is a standard developed by the
Distributed Management Task Force (**DMTF**) that provides a way to
access information about a computer's hardware. SMBIOS Specification
addresses how motherboard and system vendors present management
information about their products in a standard format through platform
firmware. The information is intended to allow generic instrumentation
to deliver this data to management applications and eliminates the need
for error prone operations such as probing system hardware for presence
detection.

<https://www.dmtf.org/standards/smbios>

## Processor Additional Information (Type 44)

The information in this structure defines the processor additional
information in case SMBIOS type 4 is not sufficient to describe
processor characteristics.

SMBIOS type 44 defines the standard header for the processor-specific
block, while the contents of processor-specific data are maintained by
processor architecture workgroups or vendors in separate documents.

The following Processor specific block provides information about the
processor use condition as identified or configured by platform
firmware.

### Processor-specific Block (Processor Use Condition Data)

<table>
<colgroup>
<col style="width: 9%" />
<col style="width: 20%" />
<col style="width: 10%" />
<col style="width: 10%" />
<col style="width: 49%" />
</colgroup>
<thead>
<tr>
<th><strong>Offset</strong></th>
<th><strong>Name</strong></th>
<th><strong>Length in Bytes</strong></th>
<th><strong>Value</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>00h</td>
<td>Block Identifier</td>
<td>1</td>
<td>01h</td>
<td><strong>Processor Use Condition Data (01h)</strong></td>
</tr>
<tr>
<td>01h</td>
<td>Block Length</td>
<td>1</td>
<td>08h</td>
<td>Length of Processor Use Condition Data structure</td>
</tr>
<tr>
<td>02h</td>
<td>Revision</td>
<td>2</td>
<td>0100h</td>
<td><p>Revision of the Processor Use Condition Data structure</p>
<p>Bits 15:8 Major revision (<strong>01h</strong>)</p>
<p>Bits 7:0 Minor revision (<strong>00h</strong>)</p></td>
</tr>
<tr>
<td>04</td>
<td>Use Condition Attribute</td>
<td>4</td>
<td>Bit Field</td>
<td><p>Bits 1:0    Processor Use Condition</p>
<p>                    00 : Client Use Condition</p>
<p>                    01 : Embedded Use Condition</p>
<p>                    10 : Industrial Use Condition</p>
<p>                    11 : Reserved</p>
<p>Bits 3:2    Temperature Range</p>
<p>                    00 : Commercial Temp Range</p>
<p>                    01 : Extended Temp Range</p>
<p>                    10 : Reserved</p>
<p>                    11 : Reserved</p>
<p>Bits 31:4   Reserved</p></td>
</tr>
</tbody>
</table>
