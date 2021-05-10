# Eleventy Paged Data Performance Example

This project provides the minimal configuration necessary to see the the number of times a single template is called when implementing the [create pages from data](https://www.11ty.dev/docs/pages-from-data/) pattern in Eleventy.

## Running

For convenience, you can run `npm run benchmark` to see the [performance output](https://www.11ty.dev/docs/debug-performance/) from Eleventy. The important thing to note is that the aggregate benchmarks for both <samp>Template Compile</samp> and <samp>Template Render</samp> were called **20 times** even though only 4 files were written.

You can see what's going by run `DEBUG=Dev:Eleventy:TemplateContent npm run build 2>&1 | grep 'rendered content'` which will you that the <samp>./src/possum.md</samp> is being called 20 times.

