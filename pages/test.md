---
layout: page
title: Testing
permalink: /test/
---

Testing4

Before you can begin to determine what the composition of a particular paragraph will be, you must first decide on an argument and a working thesis statement for your paper. What is the most important idea that you are trying to convey to your reader? The information in each paragraph must be related to that idea. In other words, your paragraphs should remind your reader that there is a recurrent relationship between your thesis and the information in each paragraph. A working thesis functions like a seed from which your paper, and your ideas, will grow. The whole process is an organic one—a natural progression from a seed to a full-blown paper where there are direct, familial relationships between all of the ideas in the paper.

The decision about what to put into your paragraphs begins with the germination of a seed of ideas; this “germination process” is better known as brainstorming. There are many techniques for brainstorming; whichever one you choose, this stage of paragraph development cannot be skipped. Building paragraphs can be like building a skyscraper: there must be a well-planned foundation that supports what you are building. Any cracks, inconsistencies, or other corruptions of the foundation can cause your whole paper to crumble.

Paragraphs are the building blocks of papers. Many students define paragraphs in terms of length: a paragraph is a group of at least five sentences, a paragraph is half a page long, etc. In reality, though, the unity and coherence of ideas among sentences is what constitutes a paragraph. A paragraph is defined as “a group of sentences or a single sentence that forms a unit” (Lunsford and Connors 116). Length and appearance do not determine whether a section in a paper is a paragraph. For instance, in some styles of writing, particularly journalistic styles, a paragraph can be just one sentence long. Ultimately, a paragraph is a sentence or group of sentences that support one main idea. In this handout, we will refer to this as the “controlling idea,” because it controls what happens in the rest of the paragraph.

# Documentation

## How do you smurf a murf?
    
Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas... 

Testing to see how paragraphs form
    
### How do many licks does a giraffe make?

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...
    
### Which Frank is?

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...
    
## Is fourteen enough really?

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas... 
    
### Is a circle an oval y/n?

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...
    
### Many mongerals manifest mountains

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...  
    
### How would you like a soda drink?

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas... 
    
#### I would very much like a soda drink.

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...  
    
### Thank you for accepting the soda drink.

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...


testing<ref>test</ref>

testing2<ref>test2</ref>

testing3<ref>test</ref>

testing4<ref>test3</ref>

testing5<ref>test4</ref>

test

test

test

test

test

test

test

test

test

test

test

test

test

test

test

test

test

test

test

test

test

test

test

test

<ol id="source-list"></ol>



{% raw %}

<script>

        document.addEventListener('DOMContentLoaded', function () {
            let refCounter = 1;
            const refElements = document.querySelectorAll('ref'); // Find all <ref> elements
            const sourceList = document.getElementById('source-list');
            const citationMap = {};  // To track unique citations and their corresponding numbers
            const citationInstances = {}; // To track all instances of each citation

            refElements.forEach(ref => {
                const citationContent = ref.innerHTML.trim();  // Get the content inside the <ref> tag

                if (citationMap[citationContent]) {
                    // It's a duplicate: increase the instance count and create a new instance number
                    const existingSourceNumber = citationMap[citationContent];
                    const instanceCount = citationInstances[citationContent].length + 1;
                    
                    // Create the citation link in the content
                    const citationLink = document.createElement('a');
                    citationLink.href = `#source${existingSourceNumber}`;  // Link to the same footer entry
                    citationLink.textContent = `[${existingSourceNumber}]`;
                    citationLink.className = 'citation-link';
                    citationLink.id = `citation${existingSourceNumber}.${instanceCount}`;  // Assign id to link back

                    // Insert citation after <ref> tag
                    ref.insertAdjacentElement('afterend', citationLink);

                    // Add this instance to the citationInstances list
                    citationInstances[citationContent].push(instanceCount);
                } else {
                    // If it's a new citation, add it to the citationMap
                    citationMap[citationContent] = refCounter;
                    citationInstances[citationContent] = [1]; // Start tracking instances

                    // Create the citation link in the content
                    const citationLink = document.createElement('a');
                    citationLink.href = `#source${refCounter}`;  // First instance links to the footer entry
                    citationLink.textContent = `[${refCounter}]`;
                    citationLink.className = 'citation-link';
                    citationLink.id = `citation${refCounter}.1`;  // Assign id to link back

                    // Insert citation after <ref> tag
                    ref.insertAdjacentElement('afterend', citationLink);

                    // Add source to the footer for unique citations
                    const listItem = document.createElement('li');
                    listItem.id = `source${refCounter}`;
                    listItem.innerHTML = citationInstances[citationContent].map(instance => {
                        return `<a href="#citation${refCounter}.${instance}" class="instance-link">${refCounter}.${instance}</a>`;
                    }).join(' ') + ` ${citationContent}`;
                    sourceList.appendChild(listItem);

                    refCounter++;
                }

                // Remove <ref> tag from content
                ref.remove();
            });

            // Update the footer with multiple instance links for each citation
            for (const citationContent in citationInstances) {
                const sourceNumber = citationMap[citationContent];
                const instances = citationInstances[citationContent];

                const listItem = document.getElementById(`source${sourceNumber}`);
                listItem.innerHTML = instances.map(instance => {
                    return `<a href="#citation${sourceNumber}.${instance}" class="instance-link">${sourceNumber}.${instance}</a>`;
                }).join(' ') + ` ${citationContent}`;
            }
        });
    
</script>
{% endraw %}        
