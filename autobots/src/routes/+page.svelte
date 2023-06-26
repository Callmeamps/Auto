<script>
	let noteData = "Note Data"
	let titleData = "Title Data"
	const notes = []
	let successful = false
	const toggleSuccess = () => {
		if (successful) {
			successful = false
		} successful = true
	}
	const saveNote = (currentNote) => {
		if (noteData && titleData) {
			let note = {title: titleData, note: currentNote}
			console.log(note)
			notes.push(note)
			console.log(notes)
			noteData = ""
			toggleSuccess()
		}
	}
</script>

<h1>{titleData}</h1>
<div class="breadcrumb">Tag</div>
<input bind:value={noteData} type="text" class="input" />
<button on:click={() => saveNote(noteData)} class="btn">save note</button>
<p>
	{noteData}
</p>

{#if (successful)}
	<div><p>success</p></div>
{/if}
