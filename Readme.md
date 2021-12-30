## Markdown Loader A markdown loader for weboack using markdown-it

### Installation
```
 npm install webpack-markdown-loaders -D
```


### Usage
```
const path = require('path')
const HtmlWebpackPlugin = require('html-webpack-plugin')


module.exports = {
	entry: {
		index: './src/js/index.js'
	},

	module: {
		rules: [
			{
				test: /\.md$/,
				use: [
				{
					loader: 'html-loader'
				},
				{
					loader: 'webpack-markdown-loader',
					options: {
                        html:true
                    }
				}],
			}

		]
	},

	plugins: [
		new HtmlWebpackPlugin({
      filename: 'index.html',
      template: './src/views/index.html',
      
		})

	]
}
```