<script lang="ts">
	import CodeMirror from 'svelte-codemirror-editor';
	import { parser } from '$lib/parser';
	import { LanguageSupport, LRLanguage } from '@codemirror/language';
	import { oneDarkTheme } from '@codemirror/theme-one-dark';
	import { vim } from '@replit/codemirror-vim';
	import { basicSetup } from 'codemirror';

	const example = LRLanguage.define({
		parser
	});

	let value = '';
</script>

<CodeMirror
	bind:value
	extensions={[vim(), basicSetup, new LanguageSupport(example)]}
	basic={false}
/>
