// Filterable fields: title, content, cover_image, narrator, mood, category, categories, tags, story_dynamic, prompt, is_favorite, is_public, word_count, avg_rating, rating_count
async function fetchStoryEntities() {
    const response = await fetch(`/api/apps/69bf1ff0347c8d582a4daf61/entities/Story`, {
        headers: {
            'api_key': 'ef0d0fbf0b38464e8ab4c70110248774', // or use await User.me() to get the API key
            'Content-Type': 'application/json'
        }
    });
    const data = await response.json();
    console.log(data);
}

// JavaScript Example: Updating an Entity
// Filterable fields: title, content, cover_image, narrator, mood, category, categories, tags, story_dynamic, prompt, is_favorite, is_public, word_count, avg_rating, rating_count
async function updateStoryEntity(entityId, updateData) {
    const response = await fetch(`/api/apps/69bf1ff0347c8d582a4daf61/entities/Story/${entityId}`, {
        method: 'PUT',
        headers: {
            'api_key': 'ef0d0fbf0b38464e8ab4c70110248774', // or use await User.me() to get the API key
            'Content-Type': 'application/json'
        },
        body: JSON.stringify(updateData)
    });
    const data = await response.json();
    console.log(data);
}
