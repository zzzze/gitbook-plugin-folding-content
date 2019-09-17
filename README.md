# gitbook-plugin-folding-content

This plugin provide a tag to create a folding content in your GitBook.

Just like this:

<details>
  <summary>He wishes for the Cloths of Heaven</summary>

  by W.B.Yeats

  > Had I the heavens’ embroidered cloths,

  > Enwrought with golden and silver light,

  > The blue and the dim and the dark cloths

  > of night and light and the half-light,

  > I would spread the cloths under your feet.

  > But I, being poor, have only my dreams;

  > I have spread my dreams under your feet,

  > Tread softly because you tread on my dreams.
</details>

## Install

Add it to your `book.json` configuration:

```json
{
  "plugins": ["folding-content"]
}
```

Add then run `install`:

```shell
gitbook install
```

## Usage

```
{% fold <parmas> %}
<content>
{% endfold %}
```

`<content>` is anything that you want it to be folded,it can be Markdown or HTML.

`<params>` can be the following options:

| param   | type    | desc |
| :------ | :------ | :----|
| summary | String  | Summary of the content |
| open    | Boolean | Open by default |
| style   | String  | Style of the details tag |

### e.g.

1. Default

  ```text
  {% fold %}
  ## He wishes for the Cloths of Heaven

  by W.B.Yeats

  > Had I the heavens’ embroidered cloths,

  > Enwrought with golden and silver light,

  > The blue and the dim and the dark cloths

  > of night and light and the half-light,

  > I would spread the cloths under your feet.

  > But I, being poor, have only my dreams;

  > I have spread my dreams under your feet,

  > Tread softly because you tread on my dreams.
  {% endfold %}
  ```

  ![image 1](./images/001.png)
  ![image 2](./images/002.png)

2. Set param

  ```text
  {% fold summary="He wishes for the Cloths of Heaven", open=true, style="background: #fafafa;padding: 10px 20px;" %}
  by W.B.Yeats

  > Had I the heavens’ embroidered cloths,

  > Enwrought with golden and silver light,

  > The blue and the dim and the dark cloths

  > of night and light and the half-light,

  > I would spread the cloths under your feet.

  > But I, being poor, have only my dreams;

  > I have spread my dreams under your feet,

  > Tread softly because you tread on my dreams.
  {% endfold %}
  ```

  ![image 3](./images/003.png)

## Demo

1. Run the following command in shell:

  ```shell
  cd demo
  gitbook install
  gitbook serve --lrport 60032
  ```

2. And then open `http://localhost:4000` in your browser.
