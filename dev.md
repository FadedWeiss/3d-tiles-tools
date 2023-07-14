- GltfPipeline.processGlb(buffer, undefined)
- 

```javascript
import { NodeIO } from '@gltf-transform/core';

const io = new NodeIO();

// Read.
let document;

document = await io.readBinary(glb);   // Uint8Array → Document


await document.transform(
	weld(),
	quantize(),
	dedup(),
    reorder({encoder: MeshoptEncoder, level: 'medium'}),

	// Custom transform.
	backfaceCulling({cull: true}),
);

```

