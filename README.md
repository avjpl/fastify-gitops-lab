# Fastify lab desired state

Initialize this repository on main before enabling the source release workflow.
The tag-triggered source workflow writes `state/current.json` and the three
`environments/*/resources.json` files. Do not hand-edit release identity here.

Generated Kubernetes JSON is valid Kubernetes configuration. Argo CD watches
only the selected environment directory, not state/current.json.

All release-related workload configuration originates in the tagged source's
scripts/render.js. Recovery uses a new source release, not a live image edit.
