<template>
    <header>
        <h1>Bitty CSS</h1>
        <p>A very small, classless CSS framework.</p>
    </header>

    <main>
        <h3>Usage</h3>
        <section>
            <h5>npm / yarn</h5>
            <pre>
npm i bitty-css
yarn add bitty-css
</pre>
            <br>
            <p>and include in your project</p>
            <br>
            <h5>CDN</h5>
            <pre>{{
`# unpkg
<link rel="stylesheet" href="https://unpkg.com/bitty-css/dist/index.min.css">

# jsDelivr
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bitty-css/dist/index.min.css">` }}</pre>
        </section>
        <section>
        </section>

        <!-- <h2>Examples</h2> -->

        <CodePreview
            :title="'Layout'"
            :code="layout"
        />

        <CodePreview
            :title="'Typography'"
            :code="typography"
        />

        <CodePreview
            :title="'Interactions'"
            :code="interactions"
        />

        <CodePreview
            :title="'Lists'"
            :code="lists"
        />

        <CodePreview
            :title="'Code'"
            :code="code"
        />

        <CodePreview
            :title="'Form'"
            :code="form"
        />

        <CodePreview
            :title="'Card'"
            :code="card"
        />

        <CodePreview
            :title="'Table'"
            :code="table"
        />
    </main>

    <footer>
        <a href="https://github.com/Kovee98/bitty-css" target="_blank">
            <img :src="githubImg" width="40"/>
        </a>
        <a href="https://www.npmjs.com/package/bitty-css" target="_blank">
            <img :src="npmImg" width="70" class="whiteify" />
        </a>
    </footer>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';
    import CodePreview from './components/CodePreview.vue';
    import githubImg from './assets/github.png';
    import npmImg from './assets/npm.png';

    export default defineComponent({
        name: 'App',
        components: {
            CodePreview
        },
        setup () {
            const layout = `
<h3>Header</h3>
<header>
    This is a header
</header>

<h3>Main</h3>
Not wrapped with <strong>main</strong> tag
<main>
    Wrapped with <strong>main</strong> tag
</main>

<h3>Section</h3>
Not wrapped with <strong>section</strong> tag
<section>
    Wrapped with <strong>section</strong> tag
</section>

<h3>Footer</h3>
<footer>
    This is a footer
</footer>
`;
            const typography = `
<h1>Title 1</h1>
<h2>Title 2</h2>
<h3>Title 3</h3>
<h4>Title 4</h4>
<h5>Title 5</h5>
<h6>Title 6</h6>
<p>
    Lorem ipsum dolor, sit amet consectetur adipisicing elit.
    Nisi vel maiores, illum ad modi facere, ab at necessitatibus
    perspiciatis neque praesentium magnam perferendis iusto tempore
    voluptatum vitae quis eaque repellendus.
</p`;
            const interactions = `
<button>Button</button>
<a href="#">Link</a>`;
            const lists = `
<ol>
    <li>Awesome</li>
    <li>Okay</li>
    <li>Ehh</li>
</ol>
<ul>
    <li>Do this thing</li>
    <li>Do another thing</li>
    <li>Don't forget this</li>
</ul>`;
            const code = `
            <pre>
.style {
    example: test;
}
</pre>`;
            const form = `
<form action="">
    <p>Name</p>
    <input type="text" id="name" placeholder="Ex: John Smith">

    <p>Phone Number</p>
    <input type="number" id="name" placeholder="(123) 456-7890">

    <p>Food</p>
    <select name="select" id="select">
        <option value="one">Pizza</option>
        <option value="two">Cheeseburger</option>
        <option value="three">Fries</option>
    </select>

    <p>Message</p>
    <textarea name="instr" id="instr" cols="30" rows="10" placeholder="Add special instructions for delivery..."></textarea>

    <div>
        <label>
            <input type="radio" name="contact" id="email">
            Email
        </label>
        <label>
            <input type="radio" name="contact" id="text" checked>
            Text
        </label>
    </div>
    <div>
        <label>
            <input type="checkbox" name="check2" id="check">
            I agree to the terms and conditions
        </label>
    </div>
    <button>Order</button>
</form>`;
            const card = `
<article>
    Typical
</article>`;
            const table = `
<table>
    <tr>
        <th>Company</th>
        <th>Contact</th>
        <th>Country</th>
    </tr>
    <tr>
        <td>Alfreds Futterkiste</td>
        <td>Maria Anders</td>
        <td>Germany</td>
    </tr>
    <tr>
        <td>Centro comercial Moctezuma</td>
        <td>Francisco Chang</td>
        <td>Mexico</td>
    </tr>
    <tr>
        <td>Ernst Handel</td>
        <td>Roland Mendel</td>
        <td>Austria</td>
    </tr>
</table>`;

            return {
                layout,
                typography,
                interactions,
                lists,
                code,
                form,
                card,
                table,
                githubImg,
                npmImg
            };
        }
    });
</script>
