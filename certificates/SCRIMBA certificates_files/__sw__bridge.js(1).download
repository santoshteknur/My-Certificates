(function(t){var e={}
function n(i){if(e[i])return e[i].exports
var r=e[i]={i,l:false,exports:{}}
t[i].call(r.exports,r,r.exports,n)
r.l=true
return r.exports}n.m=t
n.c=e
n.i=function(t){return t}
n.d=function(t,e,i){if(!n.o(t,e)){Object.defineProperty(t,e,{configurable:false,enumerable:true,get:i})}}
n.n=function(t){var e=t&&t.__esModule?function e(){return t["default"]}:function e(){return t}
n.d(e,"a",e)
return e}
n.o=function(t,e){return Object.prototype.hasOwnProperty.call(t,e)}
n.p=""
return n(n.s=14)})([function(t,e){var n={VERSION:"1.4.8"}
n.setTimeout=function(t,e){return setTimeout(function(){e()
return n.commit()},t)}
n.setInterval=function(t,e){return setInterval(function(){e()
return n.commit()},t)}
n.clearInterval=function(t){return clearInterval(t)}
n.clearTimeout=function(t){return clearTimeout(t)}
n.subclass=function(t,e){for(let n in e){let i
i=e[n]
if(e.hasOwnProperty(n)){t[n]=i}}t.prototype=Object.create(e.prototype)
t.__super__=t.prototype.__super__=e.prototype
t.prototype.initialize=t.prototype.constructor=t
return t}
n.iterable=function(t){return t?t.toArray?t.toArray():t:[]}
n.await=function(t){if(t instanceof Array){console.warn("await (Array) is deprecated - use await Promise.all(Array)")
return Promise.all(t)}else if(t&&t.then){return t}else{return Promise.resolve(t)}}
var i=/-./g
var r={}
n.toCamelCase=function(t){if(t.indexOf("-")>=0){return t.replace(i,function(t){return t.charAt(1).toUpperCase()})}else{return t}}
n.toSetter=function(t){return r[t]||(r[t]=n.toCamelCase("set-"+t))}
n.indexOf=function(t,e){return e&&e.indexOf?e.indexOf(t):[].indexOf.call(t,e)}
n.len=function(t){return t&&(t.len instanceof Function?t.len.call(t):t.length)||0}
n.prop=function(t,e,n){if(t.defineProperty){return t.defineProperty(e,n)}return}
n.attr=function(t,e,i){if(i===undefined)i={}
if(t.defineAttribute){return t.defineAttribute(e,i)}let r=n.toCamelCase(e)
let o=n.toCamelCase("set-"+e)
let s=t.prototype
if(i.dom){s[r]=function(){return this.dom()[e]}
s[o]=function(t){if(t!=this[e]()){this.dom()[e]=t}return this}}else{s[r]=function(){return this.getAttribute(e)}
s[o]=function(t){this.setAttribute(e,t)
return this}}return}
n.propDidSet=function(t,e,n,i){let r=e.watch
if(r instanceof Function){r.call(t,n,i,e)}else if((typeof r=="string"||r instanceof String)&&t[r]){t[r](n,i,e)}return}
var o=function(t,e,n){var i,r,o
while((i=n)&&(n=n.next)){if(r=n.listener){if(n.path&&r[n.path]){o=e?r[n.path].apply(r,e):r[n.path]()}else{o=e?r.apply(n,e):r.call(n)}}if(n.times&&--n.times<=0){i.next=n.next
n.listener=null}}return}
n.listen=function(t,e,n,i){var r,o,s
r=t.__listeners__||(t.__listeners__={})
o=r[e]||(r[e]={})
s=o.tail||(o.tail=o.next={})
s.listener=n
s.path=i
o.tail=s.next={}
return s}
n.once=function(t,e,i){var r=n.listen(t,e,i)
r.times=1
return r}
n.unlisten=function(t,e,n,i){var r,o
var s=t.__listeners__
if(!s){return}if(r=s[e]){while((o=r)&&(r=r.next)){if(r==n||r.listener==n){o.next=r.next
r.listener=null
break}}}return}
n.emit=function(t,e,n){var i
if(i=t.__listeners__){if(i[e]){o(e,n,i[e])}if(i.all){o(e,[e,n],i.all)}}return}
n.observeProperty=function(t,e,i,r,o){if(o&&typeof o=="object"){n.unlisten(o,"all",t,i)}if(r&&typeof r=="object"){n.listen(r,"all",t,i)}return this}
t.exports=n},function(t,e,n){var i=n(0)
i.Pointer=function t(){this._button=-1
this._event={x:0,y:0,type:"uninitialized"}
return this}
i.Pointer.prototype.button=function(){return this._button}
i.Pointer.prototype.touch=function(){return this._touch}
i.Pointer.prototype.update=function(t){this._event=t
this._dirty=true
return this}
i.Pointer.prototype.process=function(){var t=this._event
if(this._dirty){this._prevEvent=t
this._dirty=false
if(t.type=="mousedown"){this._button=t.button
if(this._touch&&this._button!=0){return}if(this._touch){this._touch.cancel()}this._touch=new i.Touch(t,this)
this._touch.mousedown(t,t)}else if(t.type=="mousemove"){if(this._touch){this._touch.mousemove(t,t)}}else if(t.type=="mouseup"){this._button=-1
if(this._touch&&this._touch.button()==t.button){this._touch.mouseup(t,t)
this._touch=null}}}else if(this._touch){this._touch.idle()}return this}
i.Pointer.prototype.x=function(){return this._event.x}
i.Pointer.prototype.y=function(){return this._event.y}},function(t,e,n){t.exports=n(11)},function(t,e,n){function i(t){return t?t.toArray?t.toArray():t:[]}var r=n(0)
n(1)
var o=["keydown","keyup","keypress","textInput","input","change","submit","focusin","focusout","focus","blur","contextmenu","selectstart","dblclick","selectionchange","mousewheel","wheel","scroll","beforecopy","copy","beforepaste","paste","beforecut","cut","dragstart","drag","dragend","dragenter","dragover","dragleave","dragexit","drop","mouseup","mousedown","mouseenter","mouseleave","mouseout","mouseover","mousemove","transitionstart","transitionend","transitioncancel","animationstart","animationiteration","animationend"]
r.EventManager=function t(e,n){var r=this
if(!n||n.constructor!==Object)n={}
var o=n.events!==undefined?n.events:[]
r._shimFocusEvents=true&&window.netscape&&e.onfocusin===undefined
r.setRoot(e)
r.setListeners([])
r.setDelegators({})
r.setDelegator(function(t){r.delegate(t)
return true})
for(let t=0,e=i(o),n=e.length;t<n;t++){r.register(e[t])}return r}
r.EventManager.prototype.root=function(t){return this._root}
r.EventManager.prototype.setRoot=function(t){this._root=t
return this}
r.EventManager.prototype.count=function(t){return this._count}
r.EventManager.prototype.setCount=function(t){this._count=t
return this}
r.EventManager.prototype.__enabled={default:false,watch:"enabledDidSet",name:"enabled"}
r.EventManager.prototype.enabled=function(t){return this._enabled}
r.EventManager.prototype.setEnabled=function(t){var e=this.enabled()
if(t!=e){this._enabled=t}if(t!=e){this.enabledDidSet&&this.enabledDidSet(t,e,this.__enabled)}return this}
r.EventManager.prototype._enabled=false
r.EventManager.prototype.listeners=function(t){return this._listeners}
r.EventManager.prototype.setListeners=function(t){this._listeners=t
return this}
r.EventManager.prototype.delegators=function(t){return this._delegators}
r.EventManager.prototype.setDelegators=function(t){this._delegators=t
return this}
r.EventManager.prototype.delegator=function(t){return this._delegator}
r.EventManager.prototype.setDelegator=function(t){this._delegator=t
return this}
var s=[]
r.EventManager.prototype.enabledDidSet=function(t){t?this.onenable():this.ondisable()
return this}
r.EventManager.bind=function(t){if(r.Events){return r.Events.autoregister(t)}else if(s.indexOf(t)==-1&&o.indexOf(t)>=0){return s.push(t)}}
r.EventManager.activate=function(){var t
if(r.Events){return r.Events}r.Events=new r.EventManager(r.document(),{events:[]})
if(false){}r.POINTER||(r.POINTER=new r.Pointer)
var e=window&&window.ontouchstart!==undefined
if(e){r.Events.listen("touchstart",function(t){return r.Touch.ontouchstart(t)})
r.Events.listen("touchmove",function(t){return r.Touch.ontouchmove(t)})
r.Events.listen("touchend",function(t){return r.Touch.ontouchend(t)})
r.Events.listen("touchcancel",function(t){return r.Touch.ontouchcancel(t)})}r.Events.register("click",function(t){if(t.timeStamp-r.Touch.LastTimestamp>r.Touch.TapTimeout){t._imbaSimulatedTap=true
var e=new r.Event(t)
e.setType("tap")
e.process()
if(e._responder&&e.defaultPrevented){return t.preventDefault()}}return r.Events.delegate(t)})
r.Events.listen("mousedown",function(t){if(t.timeStamp-r.Touch.LastTimestamp>r.Touch.TapTimeout){if(r.POINTER){return r.POINTER.update(t).process()}}})
r.Events.listen("mouseup",function(t){if(t.timeStamp-r.Touch.LastTimestamp>r.Touch.TapTimeout){if(r.POINTER){return r.POINTER.update(t).process()}}})
r.Events.register(["mousedown","mouseup"])
r.Events.register(s)
r.Events.setEnabled(true)
return r.Events}
r.EventManager.prototype.register=function(t,e){if(e===undefined)e=true
if(t instanceof Array){for(let n=0,r=i(t),o=r.length;n<o;n++){this.register(r[n],e)}return this}if(this.delegators()[t]){return this}var n=this.delegators()[t]=e instanceof Function?e:this.delegator()
if(this.enabled()){return this.root().addEventListener(t,n,true)}}
r.EventManager.prototype.autoregister=function(t){if(o.indexOf(t)==-1){return this}return this.register(t)}
r.EventManager.prototype.listen=function(t,e,n){if(n===undefined)n=true
this.listeners().push([t,e,n])
if(this.enabled()){this.root().addEventListener(t,e,n)}return this}
r.EventManager.prototype.delegate=function(t){var e=r.Event.wrap(t)
e.process()
if(this._shimFocusEvents){if(t.type=="focus"){r.Event.wrap(t).setType("focusin").process()}else if(t.type=="blur"){r.Event.wrap(t).setType("focusout").process()}}return this}
r.EventManager.prototype.create=function(t,e,n){if(!n||n.constructor!==Object)n={}
var i=n.data!==undefined?n.data:null
var o=n.source!==undefined?n.source:null
var s=r.Event.wrap({type:t,target:e})
if(i!=undefined){s.setData(i),i}if(o){s.setSource(o),o}return s}
r.EventManager.prototype.trigger=function(){return this.create.apply(this,arguments).process()}
r.EventManager.prototype.onenable=function(){for(let t=this.delegators(),e,n=0,i=Object.keys(t),r=i.length,o;n<r;n++){o=i[n]
e=t[o]
this.root().addEventListener(o,e,true)}for(let t=0,e=i(this.listeners()),n=e.length,r;t<n;t++){r=e[t]
this.root().addEventListener(r[0],r[1],r[2])}if(true){window.addEventListener("hashchange",r.commit)
window.addEventListener("popstate",r.commit)}return this}
r.EventManager.prototype.ondisable=function(){for(let t=this.delegators(),e,n=0,i=Object.keys(t),r=i.length,o;n<r;n++){o=i[n]
e=t[o]
this.root().removeEventListener(o,e,true)}for(let t=0,e=i(this.listeners()),n=e.length,r;t<n;t++){r=e[t]
this.root().removeEventListener(r[0],r[1],r[2])}if(true){window.removeEventListener("hashchange",r.commit)
window.removeEventListener("popstate",r.commit)}return this}},function(t,e,n){function i(t){return t?t.toArray?t.toArray():t:[]}var r=n(0)
var o={esc:27,tab:9,enter:13,space:32,up:38,down:40}
var s=r.Tag.prototype
s.stopModifier=function(t){return t.stop()||true}
s.preventModifier=function(t){return t.prevent()||true}
s.silenceModifier=function(t){return t.silence()||true}
s.bubbleModifier=function(t){return t.bubble(true)||true}
s.ctrlModifier=function(t){return t.event().ctrlKey==true}
s.altModifier=function(t){return t.event().altKey==true}
s.shiftModifier=function(t){return t.event().shiftKey==true}
s.metaModifier=function(t){return t.event().metaKey==true}
s.keyModifier=function(t,e){return e.keyCode()?e.keyCode()==t:true}
s.delModifier=function(t){return t.keyCode()?t.keyCode()==8||t.keyCode()==46:true}
s.selfModifier=function(t){return t.event().target==this._dom}
s.leftModifier=function(t){return t.button()!=undefined?t.button()===0:s.keyModifier(37,t)}
s.rightModifier=function(t){return t.button()!=undefined?t.button()===2:s.keyModifier(39,t)}
s.middleModifier=function(t){return t.button()!=undefined?t.button()===1:true}
s.getHandler=function(t,e){if(this[t]){return this}if(this._owner_&&this._owner_.getHandler){return this._owner_.getHandler(t,e)}}
r.Event=function t(e){this.setEvent(e)
this._bubble=true}
r.Event.prototype.event=function(t){return this._event}
r.Event.prototype.setEvent=function(t){this._event=t
return this}
r.Event.prototype.prefix=function(t){return this._prefix}
r.Event.prototype.setPrefix=function(t){this._prefix=t
return this}
r.Event.prototype.source=function(t){return this._source}
r.Event.prototype.setSource=function(t){this._source=t
return this}
r.Event.prototype.data=function(t){return this._data}
r.Event.prototype.setData=function(t){this._data=t
return this}
r.Event.prototype.responder=function(t){return this._responder}
r.Event.prototype.setResponder=function(t){this._responder=t
return this}
r.Event.wrap=function(t){return new this(t)}
r.Event.prototype.setType=function(t){this._type=t
this
return this}
r.Event.prototype.type=function(){return this._type||this.event().type}
r.Event.prototype.native=function(){return this._event}
r.Event.prototype.name=function(){return this._name||(this._name=this.type().toLowerCase().replace(/\:/g,""))}
r.Event.prototype.bubble=function(t){if(t!=undefined){this.setBubble(t)
return this}return this._bubble}
r.Event.prototype.setBubble=function(t){this._bubble=t
return this}
r.Event.prototype.stop=function(){this.setBubble(false)
return this}
r.Event.prototype.stopPropagation=function(){return this.stop()}
r.Event.prototype.halt=function(){return this.stop()}
r.Event.prototype.prevent=function(){if(this.event().preventDefault){this.event().preventDefault()}else{this.event().defaultPrevented=true}this.defaultPrevented=true
return this}
r.Event.prototype.preventDefault=function(){console.warn("Event#preventDefault is deprecated - use Event#prevent")
return this.prevent()}
r.Event.prototype.isPrevented=function(){return this.event()&&this.event().defaultPrevented}
r.Event.prototype.cancel=function(){console.warn("Event#cancel is deprecated - use Event#prevent")
return this.prevent()}
r.Event.prototype.silence=function(){this._silenced=true
return this}
r.Event.prototype.isSilenced=function(){return!!this._silenced}
r.Event.prototype.target=function(){return r.getTagForDom(this.event()._target||this.event().target)}
r.Event.prototype.responder=function(){return this._responder}
r.Event.prototype.redirect=function(t){this._redirect=t
return this}
r.Event.prototype.processHandlers=function(t,e){let n=1
let s=e.length
let u=this._bubble
let a=e.state||(e.state={})
let h
if(u){this._bubble=1}while(n<s){let s=false
let u=e[n++]
let h=null
let l=t
let c=false
if(u instanceof Array){h=u.slice(1)
c=true
u=u[0]}if(typeof u=="string"){if(o[u]){h=[o[u]]
u="key"}let e=u+"Modifier"
if(t[e]){s=true
h=(h||[]).concat([this,a])
u=t[e]}}if(typeof u=="string"){let e=t
let n=null
let i=a.context
if(i){if(i.getHandler instanceof Function){i=i.getHandler(u,this)}if(i[u]instanceof Function){u=n=i[u]
l=i}}if(!n){console.warn("event "+this.type()+": could not find '"+u+"' in context",i)}}if(u instanceof Function){if(c){for(let e=0,n=i(h),r=n.length,o;e<r;e++){o=n[e]
if(typeof o=="string"&&o[0]=="~"&&o[1]=="$"){let n=o.slice(2)
if(n=="event"){h[e]=this}else if(this[n]instanceof Function){h[e]=this[n]()}else if(t[n]instanceof Function){h[e]=t[n]()}else{console.warn("Missing special handler $"+n)}}}}let e=u.apply(l,h||[this])
if(!s){this._responder||(this._responder=t)}if(e==false){break}if(e&&!this._silenced&&e.then instanceof Function){e.then(r.commit)}}}if(this._bubble===1){this._bubble=u}return null}
r.Event.prototype.process=function(){var t=this.name()
var e="on"+(this._prefix||"")+t
var n=null
var r=this.event()._target||this.event().target
var o=r._responder||r
var s
var u
while(o){this._redirect=null
let r=o._dom?o:o._tag
if(r){if(u=r._on_){for(let e=0,n=i(u),o=n.length,s;e<o;e++){s=n[e]
if(!s){continue}let i=s[0]
if(t==s[0]&&this.bubble()){this.processHandlers(r,s)}}if(!this.bubble()){break}}if(this.bubble()&&r[e]instanceof Function){this._responder||(this._responder=r)
this._silenced=false
s=n?r[e].apply(r,n):r[e](this,this.data())}if(r.onevent){r.onevent(this)}}if(!(this.bubble()&&(o=this._redirect||(r?r.parent():o.parentNode)))){break}}this.processed()
if(s&&s.then instanceof Function){s.then(this.processed.bind(this))}return this}
r.Event.prototype.processed=function(){if(!this._silenced&&this._responder){r.emit(r,"event",[this])
r.commit(this.event())}return this}
r.Event.prototype.x=function(){return this.native().x}
r.Event.prototype.y=function(){return this.native().y}
r.Event.prototype.button=function(){return this.native().button}
r.Event.prototype.keyCode=function(){return this.native().keyCode}
r.Event.prototype.ctrl=function(){return this.native().ctrlKey}
r.Event.prototype.alt=function(){return this.native().altKey}
r.Event.prototype.shift=function(){return this.native().shiftKey}
r.Event.prototype.meta=function(){return this.native().metaKey}
r.Event.prototype.key=function(){return this.native().key}
r.Event.prototype.which=function(){return this.event().which}},function(t,e,n){function i(t){return t?t.toArray?t.toArray():t:[]}var r=n(0)
r.defineTag("fragment","element",function(t){t.createNode=function(){return r.document().createDocumentFragment()}})
r.extendTag("html",function(t){t.prototype.parent=function(){return null}})
r.extendTag("canvas",function(t){t.prototype.context=function(t){if(t===undefined)t="2d"
return this.dom().getContext(t)}})
function o(t,e,n){this._node=t
this._path=e
this._args=n
if(this._args){this._setter=r.toSetter(this._path)}}o.bind=function(t,e,n,i){let r=t._data||(t._data=new this(t,n,i))
r.bind(e,n,i)
return t}
o.prototype.bind=function(t,e,n){if(t!=this._data){this._data=t}return this}
o.prototype.getFormValue=function(){return this._setter?this._data[this._path]():this._data[this._path]}
o.prototype.setFormValue=function(t){return this._setter?this._data[this._setter](t):this._data[this._path]=t}
var s=function(t){return t&&t.splice&&t.sort}
var u=function(t,e){let n=t.length,i=0
if(n!=e.length){return false}while(i++<n){if(t[i]!=e[i]){return false}}return true}
r.extendTag("input",function(t){t.prototype.lazy=function(t){return this._lazy}
t.prototype.setLazy=function(t){this._lazy=t
return this}
t.prototype.number=function(t){return this._number}
t.prototype.setNumber=function(t){this._number=t
return this}
t.prototype.bindData=function(t,e,n){o.bind(this,t,e,n)
return this}
t.prototype.checked=function(){return this._dom.checked}
t.prototype.setChecked=function(t){if(!!t!=this._dom.checked){this._dom.checked=!!t}return this}
t.prototype.setValue=function(t,e){if(this._localValue==undefined||e==undefined){this.dom().value=this._value=t
this._localValue=undefined}return this}
t.prototype.setType=function(t){this.dom().type=this._type=t
return this}
t.prototype.value=function(){let t=this._dom.value
return this._number&&t?parseFloat(t):t}
t.prototype.oninput=function(t){let e=this._dom.value
this._localValue=e
if(this._data&&!this.lazy()&&this.type()!="radio"&&this.type()!="checkbox"){this._data.setFormValue(this.value(),this)}return}
t.prototype.onchange=function(t){this._modelValue=this._localValue=undefined
if(!this.data()){return}if(this.type()=="radio"||this.type()=="checkbox"){let t=this.checked()
let e=this._data.getFormValue(this)
let n=this._value!=undefined?this._value:this.value()
if(this.type()=="radio"){return this._data.setFormValue(n,this)}else if(this.dom().value=="on"||this.dom().value==undefined){return this._data.setFormValue(!!t,this)}else if(s(e)){let i=e.indexOf(n)
if(t&&i==-1){return e.push(n)}else if(!t&&i>=0){return e.splice(i,1)}}else{return this._data.setFormValue(n,this)}}else{return this._data.setFormValue(this.value())}}
t.prototype.onblur=function(t){return this._localValue=undefined}
t.prototype.end=function(){if(this._localValue!==undefined||!this._data){return this}let t=this._data.getFormValue(this)
if(t===this._modelValue){return this}if(!s(t)){this._modelValue=t}if(this.type()=="radio"||this.type()=="checkbox"){let e=this._value
let n=s(t)?t.indexOf(e)>=0:this.dom().value=="on"||this.dom().value==undefined?!!t:t==this._value
this.setChecked(n)}else{this._dom.value=t}return this}})
r.extendTag("textarea",function(t){t.prototype.lazy=function(t){return this._lazy}
t.prototype.setLazy=function(t){this._lazy=t
return this}
t.prototype.bindData=function(t,e,n){o.bind(this,t,e,n)
return this}
t.prototype.setValue=function(t,e){if(this._localValue==undefined||e==undefined){this.dom().value=t
this._localValue=undefined}return this}
t.prototype.oninput=function(t){let e=this._dom.value
this._localValue=e
if(this._data&&!this.lazy()){return this._data.setFormValue(this.value(),this)}}
t.prototype.onchange=function(t){this._localValue=undefined
if(this._data){return this._data.setFormValue(this.value(),this)}}
t.prototype.onblur=function(t){return this._localValue=undefined}
t.prototype.render=function(){if(this._localValue!=undefined||!this._data){return}if(this._data){let t=this._data.getFormValue(this)
this._dom.value=t!=undefined?t:""}return this}})
r.extendTag("option",function(t){t.prototype.setValue=function(t){if(t!=this._value){this.dom().value=this._value=t}return this}
t.prototype.value=function(){return this._value||this.dom().value}})
r.extendTag("select",function(t){t.prototype.bindData=function(t,e,n){o.bind(this,t,e,n)
return this}
t.prototype.setValue=function(t,e){let n=this._value
this._value=t
if(!e){this.syncValue(t)}return this}
t.prototype.syncValue=function(t){let e=this._syncValue
if(this.multiple()&&t instanceof Array){if(e instanceof Array&&u(e,t)){return this}t=t.slice()}this._syncValue=t
if(typeof t=="object"){let e=this.multiple()&&t instanceof Array
for(let n=0,r=i(this.dom().options),o=r.length,s;n<o;n++){s=r[n]
let i=s._tag?s._tag.value():s.value
if(e){s.selected=t.indexOf(i)>=0}else if(t==i){this.dom().selectedIndex=n
break}}}else{this.dom().value=t}return this}
t.prototype.value=function(){if(this.multiple()){let t=[]
for(let e=0,n=i(this.dom().selectedOptions),r=n.length,o;e<r;e++){o=n[e]
t.push(o._tag?o._tag.value():o.value)}return t}else{let t=this.dom().selectedOptions[0]
return t?t._tag?t._tag.value():t.value:null}}
t.prototype.onchange=function(t){if(this._data){return this._data.setFormValue(this.value(),this)}}
t.prototype.end=function(){if(this._data){this.setValue(this._data.getFormValue(this),1)}if(this._value!=this._syncValue){this.syncValue(this._value)}return this}})},function(t,e,n){var i=n(0)
n(7)
n(3)
i.TagManager=new i.TagManagerClass
n(9)
n(5)
n(1)
n(10)
n(4)
if(true){n(8)}if(false){}},function(t,e,n){function i(t){return t?t.toArray?t.toArray():t:[]}var r=n(0)
r.TagManagerClass=function t(){this._inserts=0
this._removes=0
this._mounted=[]
this._mountables=0
this._unmountables=0
this._unmounting=0
this}
r.TagManagerClass.prototype.mounted=function(){return this._mounted}
r.TagManagerClass.prototype.insert=function(t,e){this._inserts++
if(t&&t.mount){this.regMountable(t)}return}
r.TagManagerClass.prototype.remove=function(t,e){return this._removes++}
r.TagManagerClass.prototype.changes=function(){return this._inserts+this._removes}
r.TagManagerClass.prototype.mount=function(t){return}
r.TagManagerClass.prototype.refresh=function(t){if(t===undefined)t=false
if(false){}if(!t&&this.changes()==0){return}if(this._inserts&&this._mountables>this._mounted.length||t){this.tryMount()}if((this._removes||t)&&this._mounted.length){this.tryUnmount()}this._inserts=0
this._removes=0
return this}
r.TagManagerClass.prototype.unmount=function(t){return this}
r.TagManagerClass.prototype.regMountable=function(t){if(!(t.FLAGS&r.TAG_MOUNTABLE)){t.FLAGS|=r.TAG_MOUNTABLE
return this._mountables++}}
r.TagManagerClass.prototype.tryMount=function(){var t=0
var e=document.body
var n=e.querySelectorAll(".__mount")
for(let t=0,e=i(n),r=e.length,o;t<r;t++){o=e[t]
if(o&&o._tag){if(this._mounted.indexOf(o._tag)==-1){this.mountNode(o._tag)}}}return this}
r.TagManagerClass.prototype.mountNode=function(t){if(this._mounted.indexOf(t)==-1){this.regMountable(t)
this._mounted.push(t)
t.FLAGS|=r.TAG_MOUNTED
if(t.mount){t.mount()}}return}
r.TagManagerClass.prototype.tryUnmount=function(){this._unmounting++
var t=[]
var e=document.body
for(let e=0,n=i(this._mounted),r=n.length,o;e<r;e++){o=n[e]
if(!o){continue}if(!document.documentElement.contains(o._dom)){t.push(o)
this._mounted[e]=null}}this._unmounting--
if(t.length){this._mounted=this._mounted.filter(function(e){return e&&t.indexOf(e)==-1})
for(let e=0,n=t.length,i;e<n;e++){i=t[e]
i.FLAGS=i.FLAGS&~r.TAG_MOUNTED
if(i.unmount&&i._dom){i.unmount()}else if(i._scheduler){i.unschedule()}}}return this}},function(t,e,n){function i(t){return t?t.toArray?t.toArray():t:[]}var r={}
var o=n(0)
var s=function(t,e,n){if(e instanceof Array){for(let r=0,o=i(e),u=o.length;r<u;r++){s(t,o[r],n)}}else if(e&&e._slot_){t.removeChild(e)}else if(e!=null){let i=n?n.nextSibling:t._dom.firstChild
if(i instanceof Text&&i.textContent==e){t.removeChild(i)}else{throw"cannot remove string"}}return n}
var u=function(t,e){if(e instanceof Array){let n=0
let i=e.taglen
let r=i!=null?e.domlen=i:e.length
while(n<r){u(t,e[n++])}}else if(e&&e._dom){t.appendChild(e)}else if(e!=null&&e!==false){t.appendChild(o.createTextNode(e))}return}
var a=function(t,e,n){if(e instanceof Array){let i=0
let r=e.taglen
let o=r!=null?e.domlen=r:e.length
while(i<o){a(t,e[i++],n)}}else if(e&&e._dom){t.insertBefore(e,n)}else if(e!=null&&e!==false){t.insertBefore(o.createTextNode(e),n)}return n}
r.insertNestedAfter=function(t,e,n){var i=n?n.nextSibling:t._dom.firstChild
if(i){a(t,e,i)
return i.previousSibling}else{u(t,e)
return t._dom.lastChild}}
var h=function(t,e,n,s){var u=e.length
var a=e[u-1]
var h=[]
var l=[]
var c=[]
var f=0
var p=0
var d=false
var _
for(let r=0,o=i(n),s=o.length,u;r<s;r++){u=o[r]
if(u&&u.nodeType==3){_=e.indexOf(u.textContent)
if(_>=0){e[_]=u}d=true}else{_=e.indexOf(u)}h.push(_)
if(_==-1){t.removeChild(u)
l.push(-1)
c.push(-1)
continue}var g=h.length-2
while(g>=0){if(h[g]==-1){g--}else if(_>h[g]){break}else{g=l[g]}}l.push(g)
var m=g==-1?0:c[g]+1
if(m>f){f=m
p=r}c.push(m)}var v=[]
var y=h.length-1
while(y>=0){if(y==p&&h[y]!=-1){v[h[y]]=true
p=l[p]}y-=1}for(let n=0,u=i(e),a=u.length,h;n<a;n++){h=u[n]
if(!v[n]){if(!(h&&h._dom)){h=e[n]=o.createTextNode(h)}var T=e[n-1]
r.insertNestedAfter(t,h,T&&T._slot_||T||s)}s=h._slot_||(s&&s.nextSibling||t._dom.firstChild)}return a&&a._slot_||s}
var l=function(t,e,n,i){var r=e.length
var o=r
var s=e[r-1]
if(r==n.length&&e[0]===n[0]){while(o--){if(e[o]!==n[o]){break}}}if(o==-1){return s&&s._slot_||s||i}else{return h(t,e,n,i)}}
var c=function(t,e,n,i){var r=e.length
var o=n.length
var s=e.cache.i$
var u=0,a=r-o
while(u<o&&u<r&&e[u]===n[u]){u++}if(s>1e3&&s-r>500){e.cache.$prune(e)}if(a>0&&u==o){while(u<r){t.appendChild(e[u++])}return}else if(a>0){let i=r
while(i>u&&e[i-1]===n[i-1-a]){i--}if(a==i-u){let r=n[u]._slot_
while(u<i){t.insertBefore(e[u++],r)}return}}else if(a<0&&u==r){while(u<o){t.removeChild(n[u++])}return}else if(a<0){let i=o
while(i>u&&e[i-1+a]===n[i-1]){i--}if(a==u-i){while(u<i){t.removeChild(n[u++])}return}}else if(u==r){return}return h(t,e,n,i)}
var f=function(t,e,n,i){var r=e.taglen
var o=e.domlen||0
var s=r?e[r-1]:null
if(o>r){while(o>r){var u=e[--o]
t.removeChild(u._slot_)}}else if(r>o){let n=o?e[o-1]._slot_:i
let s=n?n.nextSibling:t._dom.firstChild
while(o<r){let n=e[o++]
s?t.insertBefore(n._slot_,s):t.appendChild(n._slot_)}}e.domlen=r
return s?s._slot_:i}
var p=function(t,e,n,o){var u=e==null||e===false
var a=n==null||n===false
if(e===n){if(u){return o}else if(e._slot_){return e._slot_}else if(e instanceof Array&&e.taglen!=null){return f(t,e,n,o)}else{return o?o.nextSibling:t._dom.firstChild}}else if(e instanceof Array){if(n instanceof Array){let r=e.static
if(r||n.static){if(r==n.static){for(let r=0,s=i(e),u=s.length;r<u;r++){o=p(t,s[r],n[r],o)}return o}else{s(t,n,o)}}else{return l(t,e,n,o)}}else if(!a){if(n._slot_){t.removeChild(n)}else{t.removeChild(o?o.nextSibling:t._dom.firstChild)}}return r.insertNestedAfter(t,e,o)}else if(!u&&e._slot_){if(!a){s(t,n,o)}return r.insertNestedAfter(t,e,o)}else if(u){if(!a){s(t,n,o)}return o}else{let i
if(n instanceof Array){s(t,n,o)}else if(n&&n._slot_){t.removeChild(n)}else if(!a){i=o?o.nextSibling:t._dom.firstChild
if(i instanceof Text&&i.textContent!=e){i.textContent=e
return i}}return r.insertNestedAfter(t,e,o)}}
o.extendTag("element",function(t){t.prototype.setChildren=function(t,e){var n=this._tree_
if(t===n&&(!t||t.taglen==undefined)){return this}if(!n&&e!=3){this.removeAllChildren()
u(this,t)}else if(e==1){let e=null
for(let r=0,o=i(t),s=o.length;r<s;r++){e=p(this,o[r],n[r],e)}}else if(e==2){return this}else if(e==3){let e=typeof t
if(e!="object"){return this.setText(t)}if(t&&t._dom){this.removeAllChildren()
this.appendChild(t)}else if(t instanceof Array){if(t._type==5&&n&&n._type==5){c(this,t,n,null)}else if(n instanceof Array){p(this,t,n,null)}else{this.removeAllChildren()
u(this,t)}}else{return this.setText(t)}}else if(e==4){f(this,t,n,null)}else if(e==5){c(this,t,n,null)}else if(t instanceof Array&&n instanceof Array){p(this,t,n,null)}else{this.removeAllChildren()
u(this,t)}this._tree_=t
return this}
t.prototype.content=function(){return this._content||this.children().toArray()}
t.prototype.setText=function(t){if(t!=this._tree_){var e=t===null||t===false?"":t;(this._text_||this._dom).textContent=e
this._text_||(this._text_=this._dom.firstChild)
this._tree_=t}return this}})
var d=o.Tag.prototype
d.setContent=d.setChildren
var _=typeof navigator!="undefined"&&(navigator.vendor||"").indexOf("Apple")==0
if(_){d.setText=function(t){if(t!=this._tree_){this._dom.textContent=t===null||t===false?"":t
this._tree_=t}return this}}},function(t,e,n){function i(t,e){return e&&e.indexOf?e.indexOf(t):[].indexOf.call(t,e)}function r(t,e){for(var n in e){if(e.hasOwnProperty(n))t[n]=e[n]}t.prototype=Object.create(e.prototype)
t.__super__=t.prototype.__super__=e.prototype
t.prototype.initialize=t.prototype.constructor=t}function o(t){return t?t.toArray?t.toArray():t:[]}var s=n(0)
s.CSSKeyMap={}
s.TAG_BUILT=1
s.TAG_SETUP=2
s.TAG_MOUNTING=4
s.TAG_MOUNTED=8
s.TAG_SCHEDULED=16
s.TAG_AWAKENED=32
s.TAG_MOUNTABLE=64
s.TAG_AUTOCLASS_GLOBALS=true
s.TAG_AUTOCLASS_LOCALS=true
s.TAG_AUTOCLASS_SVG=true
s.document=function(){return window.document}
s.root=function(){return s.getTagForDom(s.document().body)}
s.static=function(t,e,n){t._type=e
t.static=n
return t}
s.mount=function(t,e){e||(e=s.document().body)
e.appendChild(t.dom())
s.TagManager.insert(t,e)
t.scheduler().configure({events:true}).activate(false)
s.TagManager.refresh()
return t}
s.createTextNode=function(t){if(t&&t.nodeType==3){return t}return s.document().createTextNode(t)}
s.Tag=function t(e,n){this.setDom(e)
this.$=h.build(this)
this.$up=this._owner_=n
this._tree_=null
this.FLAGS=0
this.build()
this}
s.Tag.buildNode=function(){var t=s.document().createElement(this._nodeType||"div")
if(this._classes){var e=this._classes.join(" ")
if(e){t.className=e}}return t}
s.Tag.createNode=function(){var t=this._protoDom||(this._protoDom=this.buildNode())
return t.cloneNode(false)}
s.Tag.build=function(t){return new this(this.createNode(),t)}
s.Tag.dom=function(){return this._protoDom||(this._protoDom=this.buildNode())}
s.Tag.end=function(){return this.commit(0)}
s.Tag.inherit=function(t){t._protoDom=null
if(this._nodeType){t._nodeType=this._nodeType
t._classes=this._classes.slice()
if(t._flagName){return t._classes.push(t._flagName)}}else{t._nodeType=t._name
t._flagName=null
return t._classes=[]}}
s.Tag.prototype.optimizeTagStructure=function(){if(false){}var t=this.constructor
let e=Object.keys(this)
if(e.indexOf("mount")>=0){if(t._classes&&t._classes.indexOf("__mount")==-1){t._classes.push("__mount")}if(t._protoDom){t._protoDom.classList.add("__mount")}}for(let t=0,n=o(e),i=n.length,r;t<i;t++){r=n[t]
if(/^on/.test(r)){s.EventManager.bind(r.slice(2))}}return this}
s.attr(s.Tag,"accesskey")
s.attr(s.Tag,"autocapitalize")
s.attr(s.Tag,"contenteditable")
s.attr(s.Tag,"contextmenu")
s.attr(s.Tag,"dir")
s.attr(s.Tag,"draggable")
s.attr(s.Tag,"dropzone")
s.attr(s.Tag,"hidden")
s.attr(s.Tag,"inputmode")
s.attr(s.Tag,"itemid")
s.attr(s.Tag,"itemprop")
s.attr(s.Tag,"itemref")
s.attr(s.Tag,"itemscope")
s.attr(s.Tag,"itemtype")
s.attr(s.Tag,"lang")
s.attr(s.Tag,"name")
s.attr(s.Tag,"role")
s.attr(s.Tag,"slot")
s.attr(s.Tag,"spellcheck")
s.attr(s.Tag,"tabindex")
s.Tag.prototype.title=function(t){return this.getAttribute("title")}
s.Tag.prototype.setTitle=function(t){this.setAttribute("title",t)
return this}
s.attr(s.Tag,"translate")
s.Tag.prototype.dom=function(){return this._dom}
s.Tag.prototype.setDom=function(t){t._tag=this
this._dom=this._slot_=t
return this}
s.Tag.prototype.ref=function(){return this._ref}
s.Tag.prototype.root=function(){return this._owner_?this._owner_.root():this}
s.Tag.prototype.ref_=function(t){this.flag(this._ref=t)
return this}
s.Tag.prototype.setData=function(t){this._data=t
return this}
s.Tag.prototype.data=function(){return this._data}
s.Tag.prototype.bindData=function(t,e,n){return this.setData(n?t[e].apply(t,n):t[e])}
s.Tag.prototype.setHtml=function(t){if(this.html()!=t){this._dom.innerHTML=t}return this}
s.Tag.prototype.html=function(){return this._dom.innerHTML}
s.Tag.prototype.on$=function(t,e,n){let i=this._on_||(this._on_=[])
let r=i[t]
if(t<0){if(r==undefined){t=i[t]=i.length}else{t=r}r=i[t]}i[t]=e
if(r){e.state=r.state}else{e.state={context:n}
if(true){s.EventManager.bind(e[0])}}return this}
s.Tag.prototype.setId=function(t){if(t!=null){this.dom().id=t}return this}
s.Tag.prototype.id=function(){return this.dom().id}
s.Tag.prototype.setAttribute=function(t,e){var n=this.dom().getAttribute(t)
if(n==e){e}else if(e!=null&&e!==false){this.dom().setAttribute(t,e)}else{this.dom().removeAttribute(t)}return this}
s.Tag.prototype.setNestedAttr=function(t,e,n,i){if(this[t+"SetAttribute"]){this[t+"SetAttribute"](e,n,i)}else{this.setAttributeNS(t,e,n)}return this}
s.Tag.prototype.setAttributeNS=function(t,e,n){var i=this.getAttributeNS(t,e)
if(i!=n){if(n!=null&&n!==false){this.dom().setAttributeNS(t,e,n)}else{this.dom().removeAttributeNS(t,e)}}return this}
s.Tag.prototype.removeAttribute=function(t){return this.dom().removeAttribute(t)}
s.Tag.prototype.getAttribute=function(t){return this.dom().getAttribute(t)}
s.Tag.prototype.getAttributeNS=function(t,e){return this.dom().getAttributeNS(t,e)}
s.Tag.prototype.set=function(t,e,n){let i=s.toSetter(t)
if(this[i]instanceof Function){this[i](e,n)}else{this._dom.setAttribute(t,e)}return this}
s.Tag.prototype.get=function(t){return this._dom.getAttribute(t)}
s.Tag.prototype.setContent=function(t,e){this.setChildren(t,e)
return this}
s.Tag.prototype.setChildren=function(t,e){this._tree_=t
return this}
s.Tag.prototype.setTemplate=function(t){if(!this._template){if(this.render==s.Tag.prototype.render){this.render=this.renderTemplate}}this.template=this._template=t
return this}
s.Tag.prototype.template=function(){return null}
s.Tag.prototype.renderTemplate=function(){var t=this.template()
if(t!=this){this.setChildren(t)}return this}
s.Tag.prototype.removeChild=function(t){var e=this.dom()
var n=t._slot_||t
if(n&&n.parentNode==e){s.TagManager.remove(n._tag||n,this)
e.removeChild(n)}return this}
s.Tag.prototype.removeAllChildren=function(){if(this._dom.firstChild){var t
while(t=this._dom.firstChild){true&&s.TagManager.remove(t._tag||t,this)
this._dom.removeChild(t)}}this._tree_=this._text_=null
return this}
s.Tag.prototype.appendChild=function(t){if(typeof t=="string"||t instanceof String){this.dom().appendChild(s.document().createTextNode(t))}else if(t){this.dom().appendChild(t._slot_||t)
s.TagManager.insert(t._tag||t,this)}return this}
s.Tag.prototype.insertBefore=function(t,e){if(typeof t=="string"||t instanceof String){t=s.document().createTextNode(t)}if(t&&e){this.dom().insertBefore(t._slot_||t,e._slot_||e)
s.TagManager.insert(t._tag||t,this)}return this}
s.Tag.prototype.detachFromParent=function(){if(this._slot_==this._dom){this._slot_=this._dom._placeholder_||(this._dom._placeholder_=s.document().createComment("node"))
this._slot_._tag||(this._slot_._tag=this)
if(this._dom.parentNode){s.TagManager.remove(this,this._dom.parentNode)
this._dom.parentNode.replaceChild(this._slot_,this._dom)}}return this}
s.Tag.prototype.attachToParent=function(){if(this._slot_!=this._dom){let t=this._slot_
this._slot_=this._dom
if(t&&t.parentNode){s.TagManager.insert(this)
t.parentNode.replaceChild(this._dom,t)}}return this}
s.Tag.prototype.orphanize=function(){var t
if(t=this.parent()){t.removeChild(this)}return this}
s.Tag.prototype.text=function(t){return this._dom.textContent}
s.Tag.prototype.setText=function(t){this._tree_=t
this._dom.textContent=t==null||this.text()===false?"":t
this
return this}
s.Tag.prototype.dataset=function(t,e){if(t instanceof Object){for(let e,n=0,i=Object.keys(t),r=i.length,o;n<r;n++){o=i[n]
e=t[o]
this.dataset(o,e)}return this}if(arguments.length==2){this.setAttribute("data-"+t,e)
return this}if(t){return this.getAttribute("data-"+t)}var n=this.dom().dataset
if(!n){n={}
for(let t=0,e=o(this.dom().attributes),i=e.length,r;t<i;t++){r=e[t]
if(r.name.substr(0,5)=="data-"){n[s.toCamelCase(r.name.slice(5))]=r.value}}}return n}
s.Tag.prototype.render=function(){return this}
s.Tag.prototype.build=function(){return this}
s.Tag.prototype.setup=function(){return this}
s.Tag.prototype.commit=function(){if(this.beforeRender()!==false)this.render()
return this}
s.Tag.prototype.beforeRender=function(){return this}
s.Tag.prototype.tick=function(){if(this.beforeRender()!==false)this.render()
return this}
s.Tag.prototype.end=function(){this.setup()
this.commit(0)
this.end=s.Tag.end
return this}
s.Tag.prototype.$open=function(t){if(t!=this._context_){this._tree_=null
this._context_=t}return this}
s.Tag.prototype.synced=function(){return this}
s.Tag.prototype.awaken=function(){return this}
s.Tag.prototype.flags=function(){return this._dom.classList}
s.Tag.prototype.flag=function(t,e){if(arguments.length==2){if(this._dom.classList.contains(t)!=!!e){this._dom.classList.toggle(t)}}else{if(!this._dom.classList.contains(t)){this._dom.classList.add(t)}}return this}
s.Tag.prototype.unflag=function(t){this._dom.classList.remove(t)
return this}
s.Tag.prototype.toggleFlag=function(t){this._dom.classList.toggle(t)
return this}
s.Tag.prototype.hasFlag=function(t){return this._dom.classList.contains(t)}
s.Tag.prototype.flagIf=function(t,e){var n=this._flags_||(this._flags_={})
let i=n[t]
if(e&&!i){this._dom.classList.add(t)
n[t]=true}else if(i&&!e){this._dom.classList.remove(t)
n[t]=false}return this}
s.Tag.prototype.setFlag=function(t,e){let n=this._namedFlags_||(this._namedFlags_={})
let i=n[t]
if(i!=e){if(i){this.unflag(i)}if(e){this.flag(e)}n[t]=e}return this}
s.Tag.prototype.scheduler=function(){return this._scheduler==null?this._scheduler=new s.Scheduler(this):this._scheduler}
s.Tag.prototype.schedule=function(t){if(t===undefined)t={events:true}
this.scheduler().configure(t).activate()
return this}
s.Tag.prototype.unschedule=function(){if(this._scheduler){this.scheduler().deactivate()}return this}
s.Tag.prototype.parent=function(){return s.getTagForDom(this.dom().parentNode)}
s.Tag.prototype.children=function(t){let e=[]
for(let t=0,n=o(this._dom.children),i=n.length,r;t<i;t++){r=n[t]
e.push(r._tag||s.getTagForDom(r))}return e}
s.Tag.prototype.querySelector=function(t){return s.getTagForDom(this._dom.querySelector(t))}
s.Tag.prototype.querySelectorAll=function(t){var e=[]
for(let n=0,i=o(this._dom.querySelectorAll(t)),r=i.length;n<r;n++){e.push(s.getTagForDom(i[n]))}return e}
s.Tag.prototype.matches=function(t){var e
if(t instanceof Function){return t(this)}if(t.query instanceof Function){t=t.query()}if(e=this._dom.matches||this._dom.matchesSelector||this._dom.webkitMatchesSelector||this._dom.msMatchesSelector||this._dom.mozMatchesSelector){return e.call(this._dom,t)}}
s.Tag.prototype.closest=function(t){return s.getTagForDom(this._dom.closest(t))}
s.Tag.prototype.contains=function(t){return this.dom().contains(t._dom||t)}
s.Tag.prototype.log=function(){var t=arguments,e=t.length
var n=new Array(e>0?e:0)
while(e>0)n[e-1]=t[--e]
n.unshift(console)
Function.prototype.call.apply(console.log,n)
return this}
s.Tag.prototype.css=function(t,e,n){if(t instanceof Object){for(let e,n=0,i=Object.keys(t),r=i.length,o;n<r;n++){o=i[n]
e=t[o]
this.css(o,e)}return this}var i=s.CSSKeyMap[t]||t
if(e==null){this.dom().style.removeProperty(i)}else if(e==undefined&&arguments.length==1){return this.dom().style[i]}else if(i.match(/^--/)){this.dom().style.setProperty(i,e)}else{if((typeof e=="number"||e instanceof Number)&&(i.match(/width|height|left|right|top|bottom/)||n&&n.px)){this.dom().style[i]=e+"px"}else{this.dom().style[i]=e}}return this}
s.Tag.prototype.setStyle=function(t){return this.setAttribute("style",t)}
s.Tag.prototype.style=function(){return this.getAttribute("style")}
s.Tag.prototype.trigger=function(t,e){if(e===undefined)e={}
return true&&s.Events.trigger(t,this,{data:e})}
s.Tag.prototype.focus=function(){this.dom().focus()
return this}
s.Tag.prototype.blur=function(){this.dom().blur()
return this}
s.Tag.prototype.toString=function(){return this.dom().outerHTML}
s.Tag.prototype.initialize=s.Tag
s.SVGTag=function t(){return s.Tag.apply(this,arguments)}
r(s.SVGTag,s.Tag)
s.SVGTag.namespaceURI=function(){return"http://www.w3.org/2000/svg"}
s.SVGTag.buildNode=function(){var t=s.document().createElementNS(this.namespaceURI(),this._nodeType)
if(this._classes){var e=this._classes.join(" ")
if(e){t.className.baseVal=e}}return t}
s.SVGTag.inherit=function(t){t._protoDom=null
if(this==s.SVGTag){t._nodeType=t._name
return t._classes=[]}else{t._nodeType=this._nodeType
var e=(this._classes||[]).slice(0)
if(s.TAG_AUTOCLASS_SVG){e.push("_"+t._name.replace(/_/g,"-"))}return t._classes=e}}
s.HTML_TAGS="a abbr address area article aside audio b base bdi bdo big blockquote body br button canvas caption cite code col colgroup data datalist dd del details dfn div dl dt em embed fieldset figcaption figure footer form h1 h2 h3 h4 h5 h6 head header hr html i iframe img input ins kbd keygen label legend li link main map mark menu menuitem meta meter nav noscript object ol optgroup option output p param pre progress q rp rt ruby s samp script section select small source span strong style sub summary sup table tbody td textarea tfoot th thead time title tr track u ul var video wbr".split(" ")
s.HTML_TAGS_UNSAFE="article aside header section".split(" ")
s.HTML_ATTRS={a:"href target hreflang media download rel type ping referrerpolicy",audio:"autoplay controls crossorigin loop muted preload src",area:"alt coords download href hreflang ping referrerpolicy rel shape target",base:"href target",video:"autoplay buffered controls crossorigin height loop muted preload poster src width playsinline",fieldset:"disabled form name",form:"method action enctype autocomplete target",button:"autofocus type form formaction formenctype formmethod formnovalidate formtarget value name",embed:"height src type width",input:"accept disabled form list max maxlength min minlength pattern required size step type",label:"accesskey for form",img:"alt src srcset crossorigin decoding height importance intrinsicsize ismap referrerpolicy sizes width usemap",link:"rel type href media",iframe:"allow allowfullscreen allowpaymentrequest height importance name referrerpolicy sandbox src srcdoc width frameborder align longdesc scrolling",meta:"property content charset desc http-equiv color-scheme name scheme",map:"name",optgroup:"label",option:"label",output:"for form",object:"type data width height",param:"name type value valuetype",progress:"max",script:"src type async defer crossorigin integrity nonce language nomodule",select:"size form multiple",source:"sizes src srcset type media",textarea:"rows cols minlength maxlength form wrap",track:"default kind label src srclang",td:"colspan rowspan headers",th:"colspan rowspan"}
s.HTML_PROPS={input:"autofocus autocomplete autocapitalize autocorrect value placeholder required disabled multiple checked readOnly spellcheck",textarea:"autofocus autocomplete autocapitalize autocorrect value placeholder required disabled multiple checked readOnly spellcheck",form:"novalidate",fieldset:"disabled",button:"disabled",select:"autofocus disabled required readOnly multiple",option:"disabled selected value",optgroup:"disabled",progress:"value",fieldset:"disabled",canvas:"width height"}
var u=function(t,e){for(let n,i=0,r=Object.keys(e),o=r.length,s;i<o;i++){s=r[i]
n=e[s]
t[s]==null?t[s]=n:t[s]}t.prototype=Object.create(e.prototype)
t.__super__=t.prototype.__super__=e.prototype
t.prototype.constructor=t
if(e.inherit){e.inherit(t)}return t}
function a(){return function(t,e){this.initialize(t,e)
return this}}s.Tags=function t(){this}
s.Tags.prototype.__clone=function(t){var e=Object.create(this)
e._parent=this
return e}
s.Tags.prototype.ns=function(t){return this["_"+t.toUpperCase()]||this.defineNamespace(t)}
s.Tags.prototype.defineNamespace=function(t){var e=Object.create(this)
e._parent=this
e._ns=t
this["_"+t.toUpperCase()]=e
return e}
s.Tags.prototype.baseType=function(t,e){return i(t,s.HTML_TAGS)>=0?"element":"div"}
s.Tags.prototype.defineTag=function(t,e,n){if(n==undefined&&typeof e=="function")n=e,e=""
if(e==undefined)e=""
if(n&&n._nodeType){e=n
n=null}if(this[t]){console.log("tag already exists?",t)}var i
var r=t
let o=r.indexOf(":")
if(o>=0){i=t.substr(0,o)
r=t.substr(o+1)
if(i=="svg"&&!e){e="svg:element"}}e||(e=this.baseType(t))
let h=typeof e=="string"||e instanceof String?this.findTagType(e):e
let l=a()
l._name=r
l._flagName=null
if(r[0]=="#"){s.SINGLETONS[r.slice(1)]=l
this[r]=l}else if(r[0]==r[0].toUpperCase()){if(s.TAG_AUTOCLASS_LOCALS){l._flagName=r}}else{if(s.TAG_AUTOCLASS_GLOBALS){l._flagName="_"+t.replace(/[_\:]/g,"-")}this[t]=l}u(l,h)
if(n){n.call(l,l,l.TAGS||this)
if(l.defined){l.defined()}this.optimizeTag(l)}return l}
s.Tags.prototype.defineSingleton=function(t,e,n){return this.defineTag(t,e,n)}
s.Tags.prototype.extendTag=function(t,e,n){if(n==undefined&&typeof e=="function")n=e,e=""
if(e==undefined)e=""
var i=typeof t=="string"||t instanceof String?this.findTagType(t):t
if(n){n&&n.call(i,i,i.prototype)}if(i.extended){i.extended()}this.optimizeTag(i)
return i}
s.Tags.prototype.optimizeTag=function(t){var e
return(e=t.prototype)&&e.optimizeTagStructure&&e.optimizeTagStructure()}
s.Tags.prototype.findTagType=function(t){var e,n
let i=this[t]
if(!i){if(t.substr(0,4)=="svg:"){i=this.defineTag(t,"svg:element")}else if(s.HTML_TAGS.indexOf(t)>=0){i=this.defineTag(t,"element")
if(e=s.HTML_ATTRS[t]){for(let t=0,n=o(e.split(" ")),r=n.length;t<r;t++){s.attr(i,n[t])}}if(n=s.HTML_PROPS[t]){for(let t=0,e=o(n.split(" ")),r=e.length;t<r;t++){s.attr(i,e[t],{dom:true})}}}}return i}
s.createElement=function(t,e,n,i){var r=t
var o
if(t instanceof Function){r=t}else{if(null){}r=s.TAGS.findTagType(t)}if(e instanceof l){o=e.par$}else if(i instanceof s.Tag){o=i}else{o=e&&i!=undefined?e[i]:e&&e._tag||e}var u=r.build(o)
if(e instanceof l){e.i$++
u.$key=n}if(e&&n!=undefined){e[n]=u}return u}
s.createTagCache=function(t){var e=[]
e._tag=t
return e}
s.createTagMap=function(t,e,n){var i=n!=undefined?n:t._tag
var r=new l(t,e,i)
t[e]=r
return r}
s.createTagList=function(t,e,n){var i=[]
i._type=4
i._tag=n!=undefined?n:t._tag
t[e]=i
return i}
s.createTagLoopResult=function(t,e,n){var i=[]
i._type=5
i.cache={i$:0}
return i}
function h(t){this._tag=t
this}h.build=function(t){var e=[]
e._tag=t
return e}
function l(t,e,n){this.cache$=t
this.key$=e
this.par$=n
this.i$=0}l.prototype.$iter=function(){var t=[]
t._type=5
t.cache=this
return t}
l.prototype.$prune=function(t){let e=this.cache$
let n=this.key$
let i=new l(e,n,this.par$)
for(let e=0,n=o(t),r=n.length,s;e<r;e++){s=n[e]
i[s.key$]=s}i.i$=t.length
return e[n]=i}
s.TagMap=l
s.TagCache=h
s.SINGLETONS={}
s.TAGS=new s.Tags
s.TAGS.element=s.TAGS.htmlelement=s.Tag
s.TAGS["svg:element"]=s.SVGTag
s.attr(s.Tag,"is")
s.defineTag=function(t,e,n){if(n==undefined&&typeof e=="function")n=e,e=""
if(e==undefined)e=""
return s.TAGS.defineTag(t,e,n)}
s.defineSingletonTag=function(t,e,n){if(n==undefined&&typeof e=="function")n=e,e="div"
if(e==undefined)e="div"
return s.TAGS.defineTag(this.name(),e,n)}
s.extendTag=function(t,e){return s.TAGS.extendTag(t,e)}
s.getTagSingleton=function(t){var e
var n,i
if(e=s.SINGLETONS[t]){if(e&&e.Instance){return e.Instance}if(n=s.document().getElementById(t)){i=e.Instance=new e(n)
i.awaken(n)
return i}n=e.createNode()
n.id=t
i=e.Instance=new e(n)
i.end().awaken(n)
return i}else if(n=s.document().getElementById(t)){return s.getTagForDom(n)}}
var c=typeof SVGElement!=="undefined"
s.getTagForDom=function(t){if(!t){return null}if(t._dom){return t}if(t._tag){return t._tag}if(!t.nodeName){return null}var e=t.nodeName.toLowerCase()
var n=e
var i=s.TAGS
if(t.id&&s.SINGLETONS[t.id]){return s.getTagSingleton(t.id)}if(c&&t instanceof SVGElement){n=i.findTagType("svg:"+e)}else if(s.HTML_TAGS.indexOf(e)>=0){n=i.findTagType(e)}else{n=s.Tag}return new n(t,null).awaken(t)}
if(false){var f=window.getComputedStyle(document.documentElement,"")
for(let t=0,e=o(f),n=e.length,i;t<n;t++){i=e[t]
var p=i.replace(/^-(webkit|ms|moz|o|blink)-/,"")
var d=p.replace(/-(\w)/g,function(t,e){return e.toUpperCase()})
if(i!=p){if(f.hasOwnProperty(p)){continue}}s.CSSKeyMap[p]=s.CSSKeyMap[d]=i}if(!document.documentElement.classList){s.extendTag("element",function(t){t.prototype.hasFlag=function(t){return new RegExp("(^|\\s)"+t+"(\\s|$)").test(this._dom.className)}
t.prototype.addFlag=function(t){if(this.hasFlag(t)){return this}this._dom.className+=(this._dom.className?" ":"")+t
return this}
t.prototype.unflag=function(t){if(!this.hasFlag(t)){return this}var e=new RegExp("(^|\\s)*"+t+"(\\s|$)*","g")
this._dom.className=this._dom.className.replace(e,"")
return this}
t.prototype.toggleFlag=function(t){return this.hasFlag(t)?this.unflag(t):this.flag(t)}
t.prototype.flag=function(t,e){if(arguments.length==2&&!!e===false){return this.unflag(t)}return this.addFlag(t)}})}}s.Tag},function(t,e,n){function i(t){return t?t.toArray?t.toArray():t:[]}var r=n(0)
r.Touch=function t(e,n){this.setEvent(e)
this.setData({})
this.setActive(true)
this._button=e&&e.button||0
this._suppress=false
this._captured=false
this.setBubble(false)
n=n
this.setUpdates(0)
return this}
r.Touch.LastTimestamp=0
r.Touch.TapTimeout=50
var o=[]
var s=0
var u={}
r.Touch.count=function(){return s}
r.Touch.lookup=function(t){return t&&(t.__touch__||u[t.identifier])}
r.Touch.release=function(t,e){var n,i
n=u[t.identifier],delete u[t.identifier],n
i=t.__touch__,delete t.__touch__,i
return}
r.Touch.ontouchstart=function(t){for(let n=0,r=i(t.changedTouches),a=r.length,h;n<a;n++){h=r[n]
if(this.lookup(h)){continue}var e=u[h.identifier]=new this(t)
h.__touch__=e
o.push(e)
s++
e.touchstart(t,h)}return this}
r.Touch.ontouchmove=function(t){var e
for(let n=0,r=i(t.changedTouches),o=r.length,s;n<o;n++){s=r[n]
if(e=this.lookup(s)){e.touchmove(t,s)}}return this}
r.Touch.ontouchend=function(t){var e
for(let n=0,r=i(t.changedTouches),o=r.length,u;n<o;n++){u=r[n]
if(e=this.lookup(u)){e.touchend(t,u)
this.release(u,e)
s--}}return this}
r.Touch.ontouchcancel=function(t){var e
for(let n=0,r=i(t.changedTouches),o=r.length,u;n<o;n++){u=r[n]
if(e=this.lookup(u)){e.touchcancel(t,u)
this.release(u,e)
s--}}return this}
r.Touch.onmousedown=function(t){return this}
r.Touch.onmousemove=function(t){return this}
r.Touch.onmouseup=function(t){return this}
r.Touch.prototype.phase=function(t){return this._phase}
r.Touch.prototype.setPhase=function(t){this._phase=t
return this}
r.Touch.prototype.active=function(t){return this._active}
r.Touch.prototype.setActive=function(t){this._active=t
return this}
r.Touch.prototype.event=function(t){return this._event}
r.Touch.prototype.setEvent=function(t){this._event=t
return this}
r.Touch.prototype.pointer=function(t){return this._pointer}
r.Touch.prototype.setPointer=function(t){this._pointer=t
return this}
r.Touch.prototype.target=function(t){return this._target}
r.Touch.prototype.setTarget=function(t){this._target=t
return this}
r.Touch.prototype.handler=function(t){return this._handler}
r.Touch.prototype.setHandler=function(t){this._handler=t
return this}
r.Touch.prototype.updates=function(t){return this._updates}
r.Touch.prototype.setUpdates=function(t){this._updates=t
return this}
r.Touch.prototype.suppress=function(t){return this._suppress}
r.Touch.prototype.setSuppress=function(t){this._suppress=t
return this}
r.Touch.prototype.data=function(t){return this._data}
r.Touch.prototype.setData=function(t){this._data=t
return this}
r.Touch.prototype.__bubble={chainable:true,name:"bubble"}
r.Touch.prototype.bubble=function(t){return t!==undefined?(this.setBubble(t),this):this._bubble}
r.Touch.prototype.setBubble=function(t){this._bubble=t
return this}
r.Touch.prototype.timestamp=function(t){return this._timestamp}
r.Touch.prototype.setTimestamp=function(t){this._timestamp=t
return this}
r.Touch.prototype.gestures=function(t){return this._gestures}
r.Touch.prototype.setGestures=function(t){this._gestures=t
return this}
r.Touch.prototype.capture=function(){this._captured=true
this._event&&this._event.stopPropagation()
if(!this._selblocker){this._selblocker=function(t){return t.preventDefault()}
r.document().addEventListener("selectstart",this._selblocker,true)}return this}
r.Touch.prototype.isCaptured=function(){return!!this._captured}
r.Touch.prototype.extend=function(t){this._gestures||(this._gestures=[])
this._gestures.push(t)
return this}
r.Touch.prototype.redirect=function(t){this._redirect=t
return this}
r.Touch.prototype.suppress=function(){this._active=false
return this}
r.Touch.prototype.setSuppress=function(t){console.warn("Imba.Touch#suppress= is deprecated")
this._supress=t
this
return this}
r.Touch.prototype.touchstart=function(t,e){this._event=t
this._touch=e
this._button=0
this._x=e.clientX
this._y=e.clientY
this.began()
this.update()
if(t&&this.isCaptured()){t.preventDefault()}return this}
r.Touch.prototype.touchmove=function(t,e){this._event=t
this._x=e.clientX
this._y=e.clientY
this.update()
if(t&&this.isCaptured()){t.preventDefault()}return this}
r.Touch.prototype.touchend=function(t,e){this._event=t
this._x=e.clientX
this._y=e.clientY
this.ended()
r.Touch.LastTimestamp=t.timeStamp
if(this._maxdr<20){var n=new r.Event(t)
n.setType("tap")
n.process()}if(t&&this.isCaptured()){t.preventDefault()}return this}
r.Touch.prototype.touchcancel=function(t,e){return this.cancel()}
r.Touch.prototype.mousedown=function(t,e){var n=this
n._event=t
n._button=t.button
n._x=e.clientX
n._y=e.clientY
n.began()
n.update()
n._mousemove=function(t){return n.mousemove(t,t)}
r.document().addEventListener("mousemove",n._mousemove,true)
return n}
r.Touch.prototype.mousemove=function(t,e){this._x=e.clientX
this._y=e.clientY
this._event=t
if(this.isCaptured()){t.preventDefault()}this.update()
this.move()
return this}
r.Touch.prototype.mouseup=function(t,e){this._x=e.clientX
this._y=e.clientY
this.ended()
return this}
r.Touch.prototype.idle=function(){return this.update()}
r.Touch.prototype.began=function(){this._timestamp=Date.now()
this._maxdr=this._dr=0
this._x0=this._x
this._y0=this._y
var t=this.event().target
var e=null
this._sourceTarget=t&&r.getTagForDom(t)
while(t){e=r.getTagForDom(t)
if(e&&e.ontouchstart){this._bubble=false
this.setTarget(e)
this.target().ontouchstart(this)
if(!this._bubble){break}}t=t.parentNode}this._updates++
return this}
r.Touch.prototype.update=function(){var t
if(!this._active||this._cancelled){return this}var e=Math.sqrt(this.dx()*this.dx()+this.dy()*this.dy())
if(e>this._dr){this._maxdr=e}this._dr=e
if(this._redirect){if(this._target&&this._target.ontouchcancel){this._target.ontouchcancel(this)}this.setTarget(this._redirect)
this._redirect=null
if(this.target().ontouchstart){this.target().ontouchstart(this)}if(this._redirect){return this.update()}}this._updates++
if(this._gestures){for(let t=0,e=i(this._gestures),n=e.length;t<n;t++){e[t].ontouchupdate(this)}}(t=this.target())&&t.ontouchupdate&&t.ontouchupdate(this)
if(this._redirect)this.update()
return this}
r.Touch.prototype.move=function(){var t
if(!this._active||this._cancelled){return this}if(this._gestures){for(let t=0,e=i(this._gestures),n=e.length,r;t<n;t++){r=e[t]
if(r.ontouchmove){r.ontouchmove(this,this._event)}}}(t=this.target())&&t.ontouchmove&&t.ontouchmove(this,this._event)
return this}
r.Touch.prototype.ended=function(){var t
if(!this._active||this._cancelled){return this}this._updates++
if(this._gestures){for(let t=0,e=i(this._gestures),n=e.length;t<n;t++){e[t].ontouchend(this)}}(t=this.target())&&t.ontouchend&&t.ontouchend(this)
this.cleanup_()
return this}
r.Touch.prototype.cancel=function(){if(!this._cancelled){this._cancelled=true
this.cancelled()
this.cleanup_()}return this}
r.Touch.prototype.cancelled=function(){var t
if(!this._active){return this}this._cancelled=true
this._updates++
if(this._gestures){for(let t=0,e=i(this._gestures),n=e.length,r;t<n;t++){r=e[t]
if(r.ontouchcancel){r.ontouchcancel(this)}}}(t=this.target())&&t.ontouchcancel&&t.ontouchcancel(this)
return this}
r.Touch.prototype.cleanup_=function(){if(this._mousemove){r.document().removeEventListener("mousemove",this._mousemove,true)
this._mousemove=null}if(this._selblocker){r.document().removeEventListener("selectstart",this._selblocker,true)
this._selblocker=null}return this}
r.Touch.prototype.dr=function(){return this._dr}
r.Touch.prototype.dx=function(){return this._x-this._x0}
r.Touch.prototype.dy=function(){return this._y-this._y0}
r.Touch.prototype.x0=function(){return this._x0}
r.Touch.prototype.y0=function(){return this._y0}
r.Touch.prototype.x=function(){return this._x}
r.Touch.prototype.y=function(){return this._y}
r.Touch.prototype.tx=function(){this._targetBox||(this._targetBox=this._target.dom().getBoundingClientRect())
return this._x-this._targetBox.left}
r.Touch.prototype.ty=function(){this._targetBox||(this._targetBox=this._target.dom().getBoundingClientRect())
return this._y-this._targetBox.top}
r.Touch.prototype.button=function(){return this._button}
r.Touch.prototype.sourceTarget=function(){return this._sourceTarget}
r.Touch.prototype.elapsed=function(){return Date.now()-this._timestamp}
r.TouchGesture=function t(){}
r.TouchGesture.prototype.__active={default:false,name:"active"}
r.TouchGesture.prototype.active=function(t){return this._active}
r.TouchGesture.prototype.setActive=function(t){this._active=t
return this}
r.TouchGesture.prototype._active=false
r.TouchGesture.prototype.ontouchstart=function(t){return this}
r.TouchGesture.prototype.ontouchupdate=function(t){return this}
r.TouchGesture.prototype.ontouchend=function(t){return this}},function(t,e,n){(function(e){var i=n(0)
var r=false
var o=typeof window!=="undefined"?window:typeof e!=="undefined"?e:null
if(o&&o.Imba){console.warn("Imba v"+o.Imba.VERSION+" is already loaded.")
i=o.Imba}else if(o){o.Imba=i
r=true
if(o.define&&o.define.amd){o.define("imba",[],function(){return i})}}t.exports=i
if(true){n(12)
n(6)
if(r){i.EventManager.activate()}}if(false){}}).call(e,n(13))},function(t,e,n){function i(t){return t?t.toArray?t.toArray():t:[]}var r=n(0)
var o
var s
if(false){}if(true){s=window.cancelAnimationFrame||window.mozCancelAnimationFrame||window.webkitRequestAnimationFrame
o=window.requestAnimationFrame
o||(o=window.webkitRequestAnimationFrame)
o||(o=window.mozRequestAnimationFrame)
o||(o=function(t){return setTimeout(t,1e3/60)})}function u(){var t=this
t._queue=[]
t._stage=-1
t._scheduled=false
t._ticker=function(e){t._scheduled=false
return t.tick(e)}
t}u.prototype.stage=function(t){return this._stage}
u.prototype.setStage=function(t){this._stage=t
return this}
u.prototype.queue=function(t){return this._queue}
u.prototype.setQueue=function(t){this._queue=t
return this}
u.prototype.add=function(t,e){if(e||this._queue.indexOf(t)==-1){this._queue.push(t)}if(!this._scheduled){return this.schedule()}}
u.prototype.tick=function(t){var e=this._queue
if(!this._ts){this._ts=t}this._dt=t-this._ts
this._ts=t
this._queue=[]
this._stage=1
this.before()
if(e.length){for(let t=0,n=i(e),r=n.length,o;t<r;t++){o=n[t]
if(o instanceof Function){o(this._dt,this)}else if(o.tick){o.tick(this._dt,this)}}}this._stage=2
this.after()
this._stage=this._scheduled?0:-1
return this}
u.prototype.schedule=function(){if(!this._scheduled){this._scheduled=true
if(this._stage==-1){this._stage=0}o(this._ticker)}return this}
u.prototype.before=function(){return this}
u.prototype.after=function(){if(r.TagManager){r.TagManager.refresh()}return this}
r.TICKER=new u
r.SCHEDULERS=[]
r.ticker=function(){return r.TICKER}
r.requestAnimationFrame=function(t){return o(t)}
r.cancelAnimationFrame=function(t){return s(t)}
var a=0
r.commit=function(t){a++
r.emit(r,"commit",t!=undefined?[t]:undefined)
if(--a==0){r.TagManager&&r.TagManager.refresh()}return}
r.Scheduler=function t(e){var n=this
n._id=h++
n._target=e
n._marked=false
n._active=false
n._marker=function(){return n.mark()}
n._ticker=function(t){return n.tick(t)}
n._dt=0
n._frame={}
n._scheduled=false
n._timestamp=0
n._ticks=0
n._flushes=0
n.onevent=n.onevent.bind(n)
n}
var h=0
r.Scheduler.event=function(t){return r.emit(r,"event",t)}
r.Scheduler.prototype.__raf={watch:"rafDidSet",name:"raf"}
r.Scheduler.prototype.raf=function(t){return this._raf}
r.Scheduler.prototype.setRaf=function(t){var e=this.raf()
if(t!=e){this._raf=t}if(t!=e){this.rafDidSet&&this.rafDidSet(t,e,this.__raf)}return this}
r.Scheduler.prototype.__interval={watch:"intervalDidSet",name:"interval"}
r.Scheduler.prototype.interval=function(t){return this._interval}
r.Scheduler.prototype.setInterval=function(t){var e=this.interval()
if(t!=e){this._interval=t}if(t!=e){this.intervalDidSet&&this.intervalDidSet(t,e,this.__interval)}return this}
r.Scheduler.prototype.__events={watch:"eventsDidSet",name:"events"}
r.Scheduler.prototype.events=function(t){return this._events}
r.Scheduler.prototype.setEvents=function(t){var e=this.events()
if(t!=e){this._events=t}if(t!=e){this.eventsDidSet&&this.eventsDidSet(t,e,this.__events)}return this}
r.Scheduler.prototype.marked=function(t){return this._marked}
r.Scheduler.prototype.setMarked=function(t){this._marked=t
return this}
r.Scheduler.prototype.rafDidSet=function(t){if(t&&this._active)this.requestTick()
return this}
r.Scheduler.prototype.intervalDidSet=function(t){clearInterval(this._intervalId)
this._intervalId=null
if(t&&this._active){this._intervalId=setInterval(this.oninterval.bind(this),t)}return this}
r.Scheduler.prototype.eventsDidSet=function(t,e){if(this._active&&t&&!e){return r.listen(r,"commit",this,"onevent")}else if(!t&&e){return r.unlisten(r,"commit",this,"onevent")}}
r.Scheduler.prototype.active=function(){return this._active}
r.Scheduler.prototype.dt=function(){return this._dt}
r.Scheduler.prototype.configure=function(t){var e
if(t===undefined)t={}
if(t.raf!=undefined){this.setRaf(e=t.raf),e}if(t.interval!=undefined){this.setInterval(e=t.interval),e}if(t.events!=undefined){this.setEvents(e=t.events),e}return this}
r.Scheduler.prototype.mark=function(){this._marked=true
if(!this._scheduled){this.requestTick()}return this}
r.Scheduler.prototype.flush=function(){this._flushes++
this._target.tick(this)
this._marked=false
return this}
r.Scheduler.prototype.tick=function(t,e){this._ticks++
this._dt=t
if(e){this._scheduled=false}this.flush()
if(this._raf&&this._active){this.requestTick()}return this}
r.Scheduler.prototype.requestTick=function(){if(!this._scheduled){this._scheduled=true
r.TICKER.add(this)}return this}
r.Scheduler.prototype.activate=function(t){if(t===undefined)t=true
if(!this._active){this._active=true
this._commit=this._target.commit
this._target.commit=function(){return this}
this._target&&this._target.flag&&this._target.flag("scheduled_")
r.SCHEDULERS.push(this)
if(this._events){r.listen(r,"commit",this,"onevent")}if(this._interval&&!this._intervalId){this._intervalId=setInterval(this.oninterval.bind(this),this._interval)}if(t){this.tick(0)}else if(this._raf){this.requestTick()}}return this}
r.Scheduler.prototype.deactivate=function(){if(this._active){this._active=false
this._target.commit=this._commit
let t=r.SCHEDULERS.indexOf(this)
if(t>=0){r.SCHEDULERS.splice(t,1)}if(this._events){r.unlisten(r,"commit",this,"onevent")}if(this._intervalId){clearInterval(this._intervalId)
this._intervalId=null}this._target&&this._target.unflag&&this._target.unflag("scheduled_")}return this}
r.Scheduler.prototype.track=function(){return this._marker}
r.Scheduler.prototype.oninterval=function(){this.tick()
r.TagManager.refresh()
return this}
r.Scheduler.prototype.onevent=function(t){if(!this._events||this._marked){return this}if(this._events instanceof Function){if(this._events(t,this))this.mark()}else if(this._events instanceof Array){if(this._events.indexOf(t&&t.type||t)>=0){this.mark()}}else{this.mark()}return this}},function(t,e){var n
n=function(){return this}()
try{n=n||Function("return this")()||(1,eval)("this")}catch(t){if(typeof window==="object")n=window}t.exports=n},function(t,e,n){n(2)
function i(){this._sw=window.navigator.serviceWorker}e.ContainerBridge=i
i.prototype.registration=function(t){return this._registration}
i.prototype.setRegistration=function(t){this._registration=t
return this}
i.prototype.register=function(){return this.setup()}
i.prototype.log=function(){var t=arguments,e=t.length
var n=new Array(e>0?e:0)
while(e>0)n[e-1]=t[--e]
return console.log.apply(console,[].concat(["Bridge"],Array.from(n)))}
i.prototype.setup=async function(){var t=this
window.addEventListener("message",function(e){if(t._sw.controller){return t._sw.controller.postMessage(e.data)}})
t._sw.addEventListener("message",function(t){return window.parent.postMessage(t.data,"*")})
return await t.createServiceWorker()}
i.prototype.createServiceWorker=async function(){if(!this._sw){throw new Error("Service workers are not supported")}var t=await this._sw.getRegistration("/")
if(t){await t.update()}else{t=await this._sw.register("/__sw__worker.js",{scope:"/"})}return this}
var r=new i
r.register()}])
