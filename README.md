# Usage example
```ES6
	const RealDebridClient = require('node-real-debrid')
	const RD = new RealDebridClient('Your API token')

	RD.time.ISO().then(data => {
		console.log(data)
		return RD.time.get()
	}).then(data => {
		console.log(data)
		return RD.user.get()
	}).then(user => {
		console.log(user)
		return RD.settings.get()
	}).then(settings => {
		console.log(settings)
		return RD.unrestrict.check('https://openload.co/f/faqKmuLs7ro/Scappa_-_Get_Out_%5BHD%5D_%282017%29_MD_Bluray_1080p.mp4')
	}).then(result => {
		console.log(result)
		return RD.traffic.get()
	}).then(traffic => {
		console.log(traffic)
		return RD.unrestrict.link('https://openload.co/f/faqKmuLs7ro/Scappa_-_Get_Out_%5BHD%5D_%282017%29_MD_Bluray_1080p.mp4')
	}).then(data => {
		console.log(data)
		return RD.torrents.addTorrent(__dirname + '\\file.torrent')
	}).then(data => {
		console.log(data)
	}).catch(error => {
		console.log('ERROR', error)
	})
```