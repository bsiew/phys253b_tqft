# disk_gluing_sphere

Target asset: `253b_final_paper/tex_docs/figures/disk_gluing_sphere.pdf`

Policy route: hand-drawn and scanned. The live Chapter 3 TeX already looks for
this PDF with `\IfFileExists`, and the placeholder text says the final drawing
should replace it without changing the prose.

Required content:
- Three left-to-right panels.
- Left panel: an oriented disk `D^2` as a cobordism `emptyset -> S^1`.
- Middle panel: the oppositely oriented disk `\overline{D^2}` as a cobordism
  `S^1 -> emptyset`.
- Right panel: the glued closed surface `\overline{D^2} \circ D^2 \cong S^2`.
- Mark the shared boundary circle used for gluing.
- Caption should identify this as the simplest Atiyah-Segal gluing
  computation: a vector paired with a covector gives the sphere partition
  function.

Verification note: check the incoming/outgoing orientation convention against
Chapter 3 equations `eq:disk-outgoing`, `eq:disk-incoming`, and
`eq:sphere-from-disks` before marking complete.
