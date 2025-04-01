<script lang="ts">
	import { EditorView, basicSetup } from 'codemirror';

	let editor = new EditorView({
		doc: 'Start document',
		extensions: [basicSetup],
		parent: document.body
	});
</script>
