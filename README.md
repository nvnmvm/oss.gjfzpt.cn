async function operator(proxiess = []){
	const _ = lodash
	return proxies.map((p = {})=>{
		const type = _.get(p,'type')
		let network = _.get(p,'network')
		if(type==='trojan'){
			_.set(p, 'name',`${_.get(p, 'name')}[定向]`)
				_.set(p,'sin','oss.gjfzpt.cn')
				if(type==='vmess'){
					_.set(p,'name',`${_.get(p,'name')}[定向]`)
					}else if(network==='ws'){
						_.set(p,'ws-opts.headers.Host','oss.gjfzpt.cn')
					}else if(network==='http'){
						_.set(p,'http-opts.method','oss.gjfzpt.cn')
					}
		}
		return p
	})
}
