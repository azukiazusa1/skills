# CodePen Prefill rules

## Boundaries

- Share only code already validated in a local browser environment.
- Do not use CodePen as evidence that an article's claim is correct.
- Never include secrets, authorization headers, private endpoints, personal data, or production credentials.
- Do not use Prefill for samples that require a server, Node.js, a CLI, a build step, or multiple processes.
- Do not save a Pen or choose its visibility on the user's behalf.

## Panel contract

| Panel | Include | Exclude |
| --- | --- | --- |
| HTML | Elements placed inside `body` | doctype, `html`, `head`, `body`, `script`, `style` wrappers |
| CSS | Raw CSS | `style` tags |
| JavaScript | Raw JavaScript | `script` tags |

Use only the panels needed by the sample. Preserve the locally validated code.

## Launcher behavior

The bundled script writes a local HTML form whose hidden `data` field contains the JSON Prefill payload. Submitting the form sends the payload to CodePen's official Prefill endpoint and opens a populated unsaved Pen.

The endpoint is `https://codepen.io/pen/define`. If CodePen changes its API, verify the current official documentation before updating the script:

- [Post to Prefill Pen](https://blog.codepen.io/docs/api/post-to-prefill-pen/)
- [CodePen API documentation](https://blog.codepen.io/docs/api/)

Opening a local launcher in a browser is not the same as submitting it. Treat form submission as the external transfer boundary and require approval immediately before that action.
