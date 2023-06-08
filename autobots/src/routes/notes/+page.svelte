<script>
    export let data
    let editTitleBtnText = "Edit";
    let editContentBtnText = "Edit";
    let editTitle = true;
    let editContent = true;
    let display = "";
    let note = {
    title: "Title",
    content: data
    };

    console.log(data)
    

    const toggleTitleInput = () => {
        if (editTitle) {
            editTitle = false;
            editTitleBtnText = "Edit"
        } else {
            editTitle = true;
            editTitleBtnText = "Close"
        };
    };

    const toggleContentInput = () => {
        if (editContent) {
            editContent = false;
            editContentBtnText = "Edit"
        } else {
            editContent = true;
            editContentBtnText = "Close"
        };
    };

    const saveNote = () => {
        if (note.content) {
            allNotes.append(note.content)
            display = note.content
        } else {
            display = "Please write a note to save."
        };
    };
</script>

<main class="m-9">
    <div class="mx-9 my-3 px-3">
        <h1 class="h1">{note.title}</h1>
    </div>
    <div id="title-bar" class="my-auto mx-9 flex w-full">
        <button class="btn btn-sm rounded variant-ghost justify-end mx-3" on:click={toggleTitleInput}>{editTitleBtnText}</button>
        <input type="text" name="title" id="note_title" class="input rounded mx-3 {`${editTitle == false ? "hidden" : ""}`}" bind:value={note.title} placeholder="title" on:submit={toggleTitleInput}>
    </div>
    <div id="note-area" class="w-full h-full mx-9 my-3">
        <div class="my-3 w-full h-50">
            <button class="btn btn-sm rounded variant-ghost justify-end mx-3" on:click={toggleContentInput}>{editContentBtnText}</button>
            <button class="btn btn-sm rounded justify-end mx-3" on:click={saveNote}>Save</button>
        </div>
        <textarea type="text" name="content" id="content" class="textarea rounded {`${editContent == false ? "hidden" : ""}`}" bind:value={note.content}/>
        <div id="content-display" class="w-full h-full px-3">
            <p>{display}</p>
        </div>
    </div>
</main>
