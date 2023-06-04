<!DOCTYPE html><html lang="pt-BR" class="" data-primer><head><link href="https://a.slack-edge.com/d5fba4c/marketing/style/onetrust/onetrust_banner.css" rel="stylesheet" type="text/css" onload="window._cdn ? _cdn.ok(this, arguments) : null" onerror="window._cdn ? _cdn.failed(this, arguments) : null" crossorigin="anonymous"><link href="https://a.slack-edge.com/e06451a/style/libs/lato-2-compressed.css" rel="stylesheet" type="text/css" onload="window._cdn ? _cdn.ok(this, arguments) : null" onerror="window._cdn ? _cdn.failed(this, arguments) : null" crossorigin="anonymous"><link href="https://a.slack-edge.com/css/v5/style/_generic.typography.larsseit.85ad0e0bbe61bdbf62bdd9efa15a921e01033c37.css" rel="stylesheet" type="text/css" onload="window._cdn ? _cdn.ok(this, arguments) : null" onerror="window._cdn ? _cdn.failed(this, arguments) : null" crossorigin="anonymous"><link rel="canonical" href="https://slack.com">

<link rel="alternate" hreflang="en-us" href="https://slack.com">

<link rel="alternate" hreflang="en-au" href="https://slack.com/intl/en-au">

<link rel="alternate" hreflang="en-gb" href="https://slack.com/intl/en-gb">

<link rel="alternate" hreflang="en-in" href="https://slack.com/intl/en-in">

<link rel="alternate" hreflang="fr-ca" href="https://slack.com/intl/fr-ca">

<link rel="alternate" hreflang="fr-fr" href="https://slack.com/intl/fr-fr">

<link rel="alternate" hreflang="de-de" href="https://slack.com/intl/de-de">

<link rel="alternate" hreflang="es-es" href="https://slack.com/intl/es-es">

<link rel="alternate" hreflang="es-419" href="https://slack.com/intl/es-la">

<link rel="alternate" hreflang="ja-jp" href="https://slack.com/intl/ja-jp">

<link rel="alternate" hreflang="pt-br" href="https://slack.com/intl/pt-br">

<link rel="alternate" hreflang="ko-kr" href="https://slack.com/intl/ko-kr">

<link rel="alternate" hreflang="it-it" href="https://slack.com/intl/it-it">

<link rel="alternate" hreflang="zh-cn" href="https://slack.com/intl/zh-cn">

<link rel="alternate" hreflang="zh-tw" href="https://slack.com/intl/zh-tw">

<link rel="alternate" hreflang="x-default" href="https://slack.com">

<script>window.ts_endpoint_url = "https:\/\/slack.com\/beacon\/timing";(function(e) {
	var n=Date.now?Date.now():+new Date,r=e.performance||{},t=[],a={},i=function(e,n){for(var r=0,a=t.length,i=[];a>r;r++)t[r][e]==n&&i.push(t[r]);return i},o=function(e,n){for(var r,a=t.length;a--;)r=t[a],r.entryType!=e||void 0!==n&&r.name!=n||t.splice(a,1)};r.now||(r.now=r.webkitNow||r.mozNow||r.msNow||function(){return(Date.now?Date.now():+new Date)-n}),r.mark||(r.mark=r.webkitMark||function(e){var n={name:e,entryType:"mark",startTime:r.now(),duration:0};t.push(n),a[e]=n}),r.measure||(r.measure=r.webkitMeasure||function(e,n,r){n=a[n].startTime,r=a[r].startTime,t.push({name:e,entryType:"measure",startTime:n,duration:r-n})}),r.getEntriesByType||(r.getEntriesByType=r.webkitGetEntriesByType||function(e){return i("entryType",e)}),r.getEntriesByName||(r.getEntriesByName=r.webkitGetEntriesByName||function(e){return i("name",e)}),r.clearMarks||(r.clearMarks=r.webkitClearMarks||function(e){o("mark",e)}),r.clearMeasures||(r.clearMeasures=r.webkitClearMeasures||function(e){o("measure",e)}),e.performance=r,"function"==typeof define&&(define.amd||define.ajs)&&define("performance",[],function(){return r}) // eslint-disable-line
})(window);</script><script>

(function () {
	
	window.TSMark = function (mark_label) {
		if (!window.performance || !window.performance.mark) return;
		performance.mark(mark_label);
	};
	window.TSMark('start_load');

	
	window.TSMeasureAndBeacon = function (measure_label, start_mark_label) {
		if (!window.performance || !window.performance.mark || !window.performance.measure) {
			return;
		}

		performance.mark(start_mark_label + '_end');

		try {
			performance.measure(measure_label, start_mark_label, start_mark_label + '_end');
			window.TSBeacon(measure_label, performance.getEntriesByName(measure_label)[0].duration);
		} catch (e) {
			
		}
	};

	
	if ('sendBeacon' in navigator) {
		window.TSBeacon = function (label, value) {
			var endpoint_url = window.ts_endpoint_url || 'https://slack.com/beacon/timing';
			navigator.sendBeacon(
				endpoint_url + '?data=' + encodeURIComponent(label + ':' + value),
				''
			);
		};
	} else {
		window.TSBeacon = function (label, value) {
			var endpoint_url = window.ts_endpoint_url || 'https://slack.com/beacon/timing';
			new Image().src = endpoint_url + '?data=' + encodeURIComponent(label + ':' + value);
		};
	}
})();
</script><script>window.TSMark('step_load');</script><script>
(function () {
	function throttle(callback, intervalMs) {
		var wait = false;

		return function () {
			if (!wait) {
				callback.apply(null, arguments);
				wait = true;
				setTimeout(function () {
					wait = false;
				}, intervalMs);
			}
		};
	}

	function getGenericLogger() {
		return {
			warn: (msg) => {
				
				if (window.console && console.warn) return console.warn(msg);
			},
			error: (msg) => {
				if (!msg) return;

				if (window.TSBeacon) return window.TSBeacon(msg, 1);

				
				if (window.console && console.warn) return console.warn(msg);
			},
		};
	}

	function globalErrorHandler(evt) {
		if (!evt) return;

		
		var details = '';

		var node = evt.srcElement || evt.target;

		var genericLogger = getGenericLogger();

		
		
		
		
		if (node && node.nodeName) {
			var nodeSrc = '';
			if (node.nodeName === 'SCRIPT') {
				nodeSrc = node.src || 'unknown';
				var errorType = evt.type || 'error';

				
				details = `[${errorType}] from script at ${nodeSrc} (failed to load?)`;
			} else if (node.nodeName === 'IMG') {
				nodeSrc = node.src || node.currentSrc;

				genericLogger.warn(`<img> fired error with url = ${nodeSrc}`);
				return;
			}
		}

		
		if (evt.error && evt.error.stack) {
			details += ` ${evt.error.stack}`;
		}

		if (evt.filename) {
			
			var fileName = evt.filename;
			var lineNo = evt.lineno;
			var colNo = evt.colno;

			details += ` from ${fileName}`;

			
			if (lineNo) {
				details += ` @ line ${lineNo}, col ${colNo}`;
			}
		}

		var msg;

		
		if (evt.error && evt.error.stack) {
			
			msg = details;
		} else {
			
			msg = `${evt.message || ''} ${details}`;
		}

		
		if (msg && msg.replace) msg = msg.replace(/\s+/g, ' ').trim();

		if (!msg || !msg.length) {
			if (node) {
				var nodeName = node.nodeName || 'unknown';

				
				
				
				if (nodeName === 'VIDEO') {
					return;
				}

				msg = `error event from node of ${nodeName}, no message provided?`;
			} else {
				msg = 'error event fired, no relevant message or node found';
			}
		}

		var logPrefix = 'ERROR caught in js/inline/register_global_error_handler';

		msg = `${logPrefix} - ${msg}`;

		genericLogger.error(msg);
	}

	
	
	
	var capture = true;

	
	var throttledHandler = throttle(globalErrorHandler, 10000);

	window.addEventListener('error', throttledHandler, capture);
})();
</script><script type="text/javascript" crossorigin="anonymous" src="https://a.slack-edge.com/bv1-10/manifest.53ec2c8.primer.min.js" onload="window._cdn ? _cdn.ok(this, arguments) : null" onerror="window._cdn ? _cdn.failed(this, arguments) : null"></script><script type="text/javascript" crossorigin="anonymous" src="https://a.slack-edge.com/bv1-10/primer-translations_pt-BR.705dd004f968fe676aba.min.js" onload="window._cdn ? _cdn.ok(this, arguments) : null" onerror="window._cdn ? _cdn.failed(this, arguments) : null"></script><noscript><meta http-equiv="refresh" content="0; URL="></noscript><script type="text/javascript">var safe_hosts = ['app.optimizely.com', 'tinyspeck.dev.slack.com'];

if (self !== top && safe_hosts.indexOf(top.location.host) === -1) {
	window.document.write(
		'\u003Cstyle>body * {display:none !important;}\u003C/style>\u003Ca href="#" onclick=' +
			'"top.location.href=window.location.href" style="display:block !important;padding:10px">Go to Slack.com\u003C/a>'
	);
}

(function() {
	var timer;
	if (self !== top && safe_hosts.indexOf(top.location.host) === -1) {
		timer = window.setInterval(function() {
			if (window) {
				try {
					var pageEl = document.getElementById('page');
					var clientEl = document.getElementById('client-ui');
					var sectionEls = document.querySelectorAll('nav, header, section');

					pageEl.parentNode.removeChild(pageEl);
					clientEl.parentNode.removeChild(clientEl);
					for (var i = 0; i < sectionEls.length; i++) {
						sectionEls[i].parentNode.removeChild(sectionEls[i]);
					}
					window.TS = null;
					window.TD = null;
					window.clearInterval(timer);
				} catch (e) {}	
			}
		}, 200);
	}
})();</script><script src="https://cdn.cookielaw.org/scripttemplates/otSDKStub.js" data-document-language="true" data-domain-script="3bcd90cf-1e32-46d7-adbd-634f66b65b7d">window.OneTrustLoaded = true;</script><script>window.OneTrustLoaded = true;</script><script>

function bootDrift() {
	if (window.drift_loaded) return;
	if (!window.OnetrustActiveGroups || false) {
		window.drift_loaded = true;
		setTimeout(
			function() {
			window.generateNewContext = () => {
					return {
						window: {
							location: {
								hash: window.location.hash,
								host: window.location.host,
								hostname: window.location.hostname,
								href: window.location.href,
								origin: window.location.origin,
								pathname: window.location.pathname,
								port: window.location.port,
								protocol: window.location.protocol,
								search: window.location.search,
							},
							navigator: {
								language: window.navigator.language,
								browserLanguage: window.navigator.browserLanguage,
								userAgent: window.navigator.userAgent,
							},
							innerHeight: window.innerHeight,
							innerWidth: window.innerWidth,
						},
						document: {
							title: document.title,
							referrer: document.referrer,
						},
					};
				};
				window.addEventListener("resize", () => {
					const driftiframe = document.getElementById("drift-iframe");
					if (!driftiframe) return;
					driftiframe.contentWindow.postMessage({type: "driftUpdateContext", data: generateNewContext()}, "*");
				});
				window.addEventListener("scroll", (event) => {
					const driftiframe = document.getElementById("drift-iframe");
					if (!driftiframe) return;
					driftiframe.contentWindow.postMessage({type: "driftParentScroll", data: {scroll: true}, target: "drift.parentScroll"}, "*");
				});
				window.addEventListener("message", function (event) {
					const driftiframe = document.getElementById("drift-iframe");
					if (!driftiframe) return;
					if (!driftiframe.contentWindow && event.source === driftiframe.contentWindow) return;
					// on startup - pass created context into iframe
					var message = event.data;
					if (message.type === "driftIframeReady") {
						driftiframe.contentWindow.postMessage({type: "driftSetContext", data: generateNewContext()}, "*");
					}
					// on widget size change - apply new size / positioning to iframe
					if (message.type === "driftIframeResize") {
						var styles = message.data.styles;
						for (var key in styles) {
							if (!styles.hasOwnProperty(key)) {
								continue;
							}
							driftiframe.style.setProperty(key, styles[key]);
						}
					}
				});
			},
		0);
	}
}
function OptanonWrapper() {
	window.dataLayer.push({'event': 'OneTrustReady'});
	if (!Optanon.GetDomainData().ShowAlertNotice || false) {
		bootDrift();
		const bottomBannerEl = document.querySelector('.c-announcement-banner-bottom');
		if (bottomBannerEl !== null) {
			bottomBannerEl.classList.remove('c-announcement-banner-bottom-invisible');
		}

	}
	Optanon.OnConsentChanged(function() {
		bootDrift();
		const bottomBannerEl = document.querySelector('.c-announcement-banner-bottom');
		if (bottomBannerEl !== null) {
			bottomBannerEl.classList.remove('c-announcement-banner-bottom-invisible');
		}
	});
}</script><meta name="facebook-domain-verification" content="chiwsajpoybn2cnqyj9w8mvrey56m0"><script type="text/javascript">
document.addEventListener("DOMContentLoaded", function(e) {
	var gtmDataLayer = window.dataLayer || [];
	var gtmTags = document.querySelectorAll('*[data-gtm-click]');
	var gtmClickHandler = function(c) {
		var gtm_events = this.getAttribute('data-gtm-click');
		if (!gtm_events) return;
		var gtm_events_arr = gtm_events.split(",");
		for(var e=0; e < gtm_events_arr.length; e++) {
			var ev = gtm_events_arr[e].trim();
			gtmDataLayer.push({ 'event': ev });
		}
	};
	for(var g=0; g < gtmTags.length; g++){
		var elem = gtmTags[g];
		elem.addEventListener('click', gtmClickHandler);
	}
});
</script><script type="text/javascript">
(function(e,c,b,f,d,g,a){e.SlackBeaconObject=d;
e[d]=e[d]||function(){(e[d].q=e[d].q||[]).push([1*new Date(),arguments])};
e[d].l=1*new Date();g=c.createElement(b);a=c.getElementsByTagName(b)[0];
g.async=1;g.src=f;a.parentNode.insertBefore(g,a)
})(window,document,"script","https://a.slack-edge.com/bv1-10/slack_beacon.84507d82b617deecde7a.min.js","sb");
window.sb('set', 'token', '3307f436963e02d4f9eb85ce5159744c');
window.sb('track', 'pageview');
</script><script type="text/javascript">var TS_last_log_date = null;
var TSMakeLogDate = function() {
	var date = new Date();

	var y = date.getFullYear();
	var mo = date.getMonth()+1;
	var d = date.getDate();

	var time = {
	  h: date.getHours(),
	  mi: date.getMinutes(),
	  s: date.getSeconds(),
	  ms: date.getMilliseconds()
	};

	Object.keys(time).map(function(moment, index) {
		if (moment == 'ms') {
			if (time[moment] < 10) {
				time[moment] = time[moment]+'00';
			} else if (time[moment] < 100) {
				time[moment] = time[moment]+'0';
			}
		} else if (time[moment] < 10) {
			time[moment] = '0' + time[moment];
		}
	});

	var str = y + '/' + mo + '/' + d + ' ' + time.h + ':' + time.mi + ':' + time.s + '.' + time.ms;
	if (TS_last_log_date) {
		var diff = date-TS_last_log_date;
		//str+= ' ('+diff+'ms)';
	}
	TS_last_log_date = date;
	return str+' ';
}

var parseDeepLinkRequest = function(code) {
	var m = code.match(/"id":"([CDG][A-Z0-9]{8,})"/);
	var id = m ? m[1] : null;

	m = code.match(/"team":"(T[A-Z0-9]{8,})"/);
	var team = m ? m[1] : null;

	m = code.match(/"message":"([0-9]+\.[0-9]+)"/);
	var message = m ? m[1] : null;

	return { id: id, team: team, message: message };
}

if ('rendererEvalAsync' in window) {
	var origRendererEvalAsync = window.rendererEvalAsync;
	window.rendererEvalAsync = function(blob) {
		try {
			var data = JSON.parse(decodeURIComponent(atob(blob)));
			if (data.code.match(/handleDeepLink/)) {
				var request = parseDeepLinkRequest(data.code);
				if (!request.id || !request.team || !request.message) return;

				request.cmd = 'channel';
				TSSSB.handleDeepLinkWithArgs(JSON.stringify(request));
				return;
			} else {
				origRendererEvalAsync(blob);
			}
		} catch (e) {
		}
	}
}</script><script type="text/javascript">var TSSSB = {
	call: function() {
		return false;
	}
};</script><title>Slack</title><meta name="referrer" content="no-referrer"><meta name="superfish" content="nofish"><meta name="author" content="Slack"><meta name="description" content=""><meta name="keywords" content=""></head><body class="full_height"><div id="page_contents"><div id="props_node" data-props="{&quot;loggedInTeams&quot;:[],&quot;entryPoint&quot;:&quot;&quot;,&quot;isPaidTeam&quot;:false,&quot;teamName&quot;:&quot;BigOil&quot;,&quot;teamDomain&quot;:&quot;bigoil-ica&quot;,&quot;encodedTeamId&quot;:&quot;TUQM1H023&quot;,&quot;emailJustSent&quot;:false,&quot;shouldRedirect&quot;:true,&quot;redirectURL&quot;:&quot;\/files-pri\/TUQM1H023-F04KZNVSA3S\/readme.md&quot;,&quot;redirectQs&quot;:&quot;\/?redir=%2Ffiles-pri%2FTUQM1H023-F04KZNVSA3S%2Freadme.md&quot;,&quot;remember&quot;:false,&quot;hasRemember&quot;:true,&quot;noSSO&quot;:false,&quot;crumbValue&quot;:&quot;s-1673977684-62fc7220015cbc1205a9026485aa4b2192f2678741f438d8c6475588fd38ea8f-\u2603&quot;,&quot;isSSB&quot;:false,&quot;isSSBSignIn&quot;:false,&quot;isSSBSonicSignIn&quot;:false,&quot;SSBVersion&quot;:&quot;&quot;,&quot;hasEmailError&quot;:false,&quot;emailValue&quot;:&quot;&quot;,&quot;hasPasswordError&quot;:false,&quot;isMobileBrowser&quot;:false,&quot;hasAuthReloginFlow&quot;:false,&quot;hasRateLimit&quot;:false,&quot;recaptchaSitekey&quot;:&quot;6LcQQiYUAAAAADxJHrihACqD5wf3lksm9jbnRY5k&quot;,&quot;hasSmsRateLimit&quot;:false,&quot;forgotPasswordLink&quot;:&quot;\/forgot&quot;,&quot;showSignupEmailLink&quot;:true,&quot;getStartedLink&quot;:&quot;https:\/\/slack.com\/get-started#\/find&quot;,&quot;loggedOutPasswordResetSentAddress&quot;:&quot;&quot;,&quot;isSSOAuthMode&quot;:false,&quot;isNormalAuthMode&quot;:true,&quot;signinUrl&quot;:&quot;https:\/\/slack.com\/signin&quot;,&quot;signinFindUrl&quot;:&quot;https:\/\/slack.com\/signin\/find&quot;,&quot;ssbRelogin&quot;:&quot;&quot;,&quot;isLoggedOut2fa&quot;:false,&quot;isLoggedOutTeam2fa&quot;:false,&quot;isLoggedOutSelfPasswordReset&quot;:false,&quot;isLoggedOutPasswordReset&quot;:false,&quot;isLoggedOutGodPasswordReset&quot;:false,&quot;isLoggedOutOwnerPasswordReset&quot;:false,&quot;isLoggedOutOwnerSSOReset&quot;:false,&quot;isLoggedOutSSOMaybeRequired&quot;:false,&quot;isLoggedOutRedirect&quot;:true,&quot;teamAuthMode&quot;:null,&quot;authModeGoogle&quot;:&quot;google&quot;,&quot;samlProviderLabel&quot;:null,&quot;errorSource&quot;:&quot;&quot;,&quot;errorMissing&quot;:false,&quot;errorNoUser&quot;:false,&quot;errorDeleted&quot;:false,&quot;errorPassword&quot;:false,&quot;errorSSONoOwner&quot;:false,&quot;errorSSONonRA&quot;:false,&quot;errorTwoFactorWrong&quot;:false,&quot;errorSmsRateLimit&quot;:false,&quot;errorConfirmed&quot;:false,&quot;errorNoPassword&quot;:false,&quot;errorTwoFactorState&quot;:false,&quot;hasEmailOnDomain&quot;:false,&quot;truncatedEmailDomains&quot;:null,&quot;truncatedEmailDomainsCount&quot;:0,&quot;formattedEmailDomains&quot;:&quot;&quot;,&quot;isReloginFlow&quot;:false,&quot;downloadLinkSigninCTA&quot;:{&quot;linkUrl&quot;:&quot;\/get-started#\/create&quot;,&quot;isDownload&quot;:false},&quot;twoFactorRequired&quot;:false,&quot;usingBackup&quot;:null,&quot;twoFactorType&quot;:null,&quot;twoFactorBackupType&quot;:null,&quot;twoFactorRequiredML&quot;:null,&quot;authcodeInputType&quot;:&quot;text&quot;,&quot;backupPhoneNumber&quot;:null,&quot;forgotPasswordError&quot;:&quot;&quot;,&quot;resetLinkSent&quot;:false,&quot;userOauth&quot;:{&quot;apple&quot;:{&quot;enabled&quot;:true,&quot;redirect_url&quot;:&quot;https:\/\/bigoil-ica.slack.com\/workspace-signin\/oauth\/apple\/start?redir=%2Ffiles-pri%2FTUQM1H023-F04KZNVSA3S%2Freadme.md&amp;is_ssb_browser_signin=&quot;},&quot;google&quot;:{&quot;enabled&quot;:true,&quot;redirect_url&quot;:&quot;https:\/\/bigoil-ica.slack.com\/workspace-signin\/oauth\/google\/start?redir=%2Ffiles-pri%2FTUQM1H023-F04KZNVSA3S%2Freadme.md&amp;is_ssb_browser_signin=&quot;}},&quot;isUrgentBannerExpOn&quot;:false,&quot;isWarningBannerExpOn&quot;:false,&quot;experimentImproveJoinerSignUpPageOnGroupOn&quot;:true,&quot;signInWithPassword&quot;:false}"></div></div><script type="text/javascript">
/**
 * A placeholder function that the build script uses to
 * replace file paths with their CDN versions.
 *
 * @param {String} file_path - File path
 * @returns {String}
 */
function vvv(file_path) {
		 var vvv_warning = 'You cannot use vvv on dynamic values. Please make sure you only pass in static file paths.'; if (window.TS && window.TS.warn) { window.TS.warn(vvv_warning); } else { console.warn(vvv_warning); } 
	return file_path;
}

var cdn_url = "https:\/\/a.slack-edge.com";
var vvv_abs_url = "https:\/\/slack.com\/";
var inc_js_setup_data = {
	emoji_sheets: {
		apple: 'https://a.slack-edge.com/80588/img/emoji_2017_12_06/sheet_apple_64_indexed_256.png',
		google: 'https://a.slack-edge.com/80588/img/emoji_2017_12_06/sheet_google_64_indexed_256.png',
	},
};
</script><script nonce="" type="text/javascript">	// common boot_data
	var boot_data = {"cdn":{"edges":["https:\/\/a.slack-edge.com\/","https:\/\/b.slack-edge.com\/","https:\/\/a.slack-edge.com\/"],"avatars":"https:\/\/ca.slack-edge.com\/","downloads":"https:\/\/downloads.slack-edge.com\/","files":"https:\/\/slack-files.com\/"},"feature_builder_story_step":false,"feature_chime_access_check":false,"feature_day2_share_modal":true,"feature_tinyspeck":false,"feature_olug_esc_channels_work":true,"feature_olug_remove_required_workspace_setting":false,"feature_data_table_in_org_level_user_groups":false,"feature_org_settings_m11n":false,"feature_deprecate_get_member_by_name":false,"feature_add_message_perf":false,"feature_print_pdf":false,"feature_desktop460_deprecation":false,"feature_desktop460_deprecation_block":false,"feature_composer_email_classification":false,"feature_amazon_a11y_custom_status_emoji":true,"feature_file_threads":true,"feature_broadcast_indicator":true,"feature_new_replies_after_bcast":true,"feature_sonic_emoji":true,"feature_emoji_12":false,"feature_attachments_inline":false,"feature_desktop_symptom_events":false,"feature_data_residency_debugging":false,"feature_ent_admin_approved_apps_v2":true,"feature_shared_channels_multi_org_qa_limit_override":false,"feature_gdpr_user_join_tos":true,"feature_user_invite_tos_april_2018":true,"feature_enrich_fetch_team_user_from_db":true,"feature_channel_mgmt_message_count":false,"feature_whitelist_zendesk_chat_widget":false,"feature_use_imgproxy_resizing":true,"feature_boards_in_dev":false,"feature_disable_bk_in_thread":true,"feature_channel_exports":false,"feature_docs_mentions_and_channels":false,"feature_calls_survey_request_response":true,"feature_sidebar_theme_undo":true,"feature_allow_intra_word_formatting":true,"feature_slim_scrollbar":false,"feature_primary_search":false,"feature_edge_upload_proxy_check":true,"feature_unread_counts_delay":true,"feature_legacy_file_upload_analytics":true,"feature_mpdm_limit_channel_creation":false,"feature_snippet_modes_i18n":false,"feature_ms_latest":true,"feature_rooms_join_url":false,"feature_custom_status_calendar_sync_copy":true,"feature_custom_status_calendar_sync":true,"feature_mask_undocumented_errors":false,"feature_app_views_reminders":true,"feature_reminders_org_shard":false,"feature_reminders_grid_migrations_org_shard":false,"feature_blocks_reminders_list":false,"feature_share_message_via_message_blocks":false,"feature_message_blocks":false,"feature_set_tz_automatically":true,"feature_confirm_clear_all_unreads_pref":true,"feature_block_mounts":true,"feature_attachments_v2":true,"feature_group_block":false,"feature_show_block_kit_in_share_dialogs":false,"feature_block_kit_range_datepicker":false,"feature_delete_app_homes_associated_with_deleted_service":true,"feature_soft_delete_app_homes_on_user_deactivation":false,"feature_beacon_js_errors":false,"feature_user_app_disable_speed_bump":true,"feature_apps_manage_permissions_scope_changes":true,"feature_reminder_cross_workspace":true,"feature_p2p":false,"feature_pages_example":false,"feature_iap1":false,"feature_ia_ga":true,"feature_ia_i18n":true,"feature_ia_member_profile":true,"feature_workspace_scim_management":false,"feature_desktop_reload_on_generic_error":true,"feature_desktop_extend_app_menu":true,"feature_desktop_restart_service_worker":false,"feature_desktop_system_notification_playback":false,"feature_bots_not_members":true,"feature_wta_stop_creation":true,"feature_platform_deprecations_fe":true,"feature_app_manifest_open_beta":true,"feature_no_socket_mode":false,"feature_no_callback_id_edit":false,"feature_admin_email_change_confirm":true,"feature_channel_actions":true,"feature_screen_share_needs_aero":false,"feature_emoji_by_id":true,"feature_channel_invite_tokenization":true,"feature_email_notify":false,"feature_improved_email_rendering":true,"feature_mini_browser_translations":false,"feature_unfurl_metadata":false,"feature_paperclip_coachmark_experiments":true,"feature_plus_menu_add_apps_link":false,"feature_recent_files_omnipicker":false,"feature_recent_desktop_files":true,"feature_huddles_i18n":false,"feature_connect_deeplink":false,"feature_cea_allowlist_changes":false,"feature_cea_channel_management":true,"feature_cea_admin_controls":false,"feature_cea_allowlist_changes_plus":false,"feature_ia_layout":true,"feature_misc_ia_a11y_translations":false,"feature_threaded_call_block":false,"feature_enable_read_time_validations_for_shortcuts":true,"feature_enterprise_mobile_device_check":true,"feature_new_copy_for_identity_basic":false,"feature_trace_webapp_init":true,"feature_trace_jq_init":true,"feature_seven_days_email_update":true,"feature_uae_tax_id_collection":true,"feature_quebec_tax_id_collection":true,"feature_quebec_tax_assessment":true,"feature_georgia_tax_id_collection":true,"feature_georgia_tax_assessment":true,"feature_liechtenstein_tax_id_collection":true,"feature_liechtenstein_tax_assessment":true,"feature_ksa_tax_id_collection":true,"feature_indonesia_tax_change_notification":false,"feature_indonesia_tax_assessment":false,"feature_channel_sections":true,"feature_channel_sections_sidebar_behavior_ui":false,"feature_migrate_google_directory_apis":true,"feature_show_email_forwarded_by":false,"feature_download_finder_update":true,"feature_share_modal_dialog":true,"feature_block_files_esc":true,"feature_invite_new_error":true,"feature_mpdm_audience_expansion":true,"feature_idr_s3_files_sharded_backfill":true,"feature_xws_user_groups_selector":true,"feature_accessible_date_picker_select":false,"feature_remove_email_preview_link":true,"feature_desktop_enable_tslog":false,"feature_desktop_enable_sticky_notification_pref":false,"feature_ntlm_domain_approval_ui":false,"feature_email_determine_charset":true,"feature_windows7_deprecation":true,"feature_windows7_deprecation_modal":false,"feature_no_deprecation_in_updater":false,"feature_user_prefers_paused_animations":true,"feature_ez_subscribe_v_1_stage_0":false,"feature_pea_domain_allowlist":true,"feature_composer_auth_admin":true,"feature_ukraine_tax_id_collection":true,"feature_ukraine_tax_assessment":true,"feature_hermes_just_in_time_auth":true,"feature_taiwan_tax_id_collection":true,"feature_uk_eu_tax_id_collection":true,"feature_uk_eu_tax_assessment":true,"experiment_assignments":{"integrity_res_legacy_or_new":{"experiment_id":"3865674806886","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1660029951,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"newxp_8307":{"experiment_id":"4452787076135","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1671206625,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"activation_browser_deprecation_warning_december_2022":{"experiment_id":"4480826650981","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1671040826,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"proj_brand_customer_stories_lp":{"experiment_id":"3448021380448","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1653596127,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"grb_v_2":{"experiment_id":"4321730126964","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1670538010,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"ssp_migration_trace":{"experiment_id":"4260895763510","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1669225936,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"promo_partners_reboot":{"experiment_id":"4274154926390","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1668724066,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"exp_mobile_focused_hp":{"experiment_id":"4100539910737","type":"visitor","group":"control","trigger":"finished","log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"deny_russian_ip":{"experiment_id":"3201051153989","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1647958022,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"de_banner_nov_22":{"experiment_id":"4281335493538","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1667492958,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"marketing_optimizely_toggle":{"experiment_id":"4238655504181","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1666828274,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"marketing_lambda_resources_2":{"experiment_id":"4244853787989","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1666643517,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"day1_simplify_get_started_landing":{"experiment_id":"3906816848548","type":"visitor","group":"control","trigger":"finished","log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"newxp_cookies":{"experiment_id":"910174584307","type":"visitor","group":"dedupe_teams","trigger":"launch_visitor","schedule_ts":1580235926,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"commingled_workspaces_v2":{"experiment_id":"3887215349444","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1659541233,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"ca_paid_vs_free_web_lp":{"experiment_id":"3664945267108","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1658149170,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"govslack_provision_block":{"experiment_id":"3289482788501","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1650990072,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"grb_lp":{"experiment_id":"4094127126097","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1663878259,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"memoize_supercookie":{"experiment_id":"3276036784741","type":"visitor","group":"on","trigger":"finished","log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"dhq_huddles_dreamforce_launch":{"experiment_id":"3984379366983","type":"visitor","group":"treatment","trigger":"launch_visitor","schedule_ts":1663676278,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"pxp214_2_v":{"experiment_id":"3583633966006","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1662037486,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"whats_new_copy_aug":{"experiment_id":"3932231708548","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1661869053,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"marketing_sc_rum_integration":{"experiment_id":"2491795733043","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1631738368,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"act_joiner_delight":{"experiment_id":"3904915634145","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1660950028,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"privacy_ireland_address":{"experiment_id":"3938303947301","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1661191091,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"privacy_policy_2022_update":{"experiment_id":"3843227279031","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1659978822,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"exp_new_workspace_module_copy":{"experiment_id":"3433334068800","type":"visitor","group":"control","trigger":"finished","log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"integrity_check_team_creation_blocking_blocklists_only":{"experiment_id":"3819669148582","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1658943718,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"self_serve_update":{"experiment_id":"3723754984774","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1658865489,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"partner_amex":{"experiment_id":"2343797778564","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1632866184,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"integrity_check_team_creation_nonblocking_visitor":{"experiment_id":"3751318743473","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1656545423,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"marketing_copy_localization":{"experiment_id":"3717980195040","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1656534241,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"search_zd_vs_solr":{"experiment_id":"1355709002145","type":"visitor","group":"control","trigger":"finished","log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"slack_connect_skip_team_name_visitor_experiment":{"experiment_id":"2158999239729","type":"visitor","group":"treatment","trigger":"finished","log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"digital_first_lightning_strike_custacq":{"experiment_id":"2220660679364","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1625075563,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"cust_acq_partners_template":{"experiment_id":"2232204551504","type":"visitor","group":"treatment","trigger":"launch_visitor","schedule_ts":1628191410,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"community_launch":{"experiment_id":"2652841576373","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1635871147,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"customer_awards_launch":{"experiment_id":"2673548411155","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1637079544,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"apidocs_f_public":{"experiment_id":"2723240261908","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1637027010,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"hc_ideas_templates_section":{"experiment_id":"2861849381797","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1640117154,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"cust_acq_nav_animation":{"experiment_id":"3082669699267","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1646259562,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"ssb_beta_signup_via_deep_link":{"experiment_id":"2736521995972","type":"visitor","group":"on","trigger":"finished","log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"slack_vs_email_lp":{"experiment_id":"3150600239841","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1652220854,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"app_directory_aws_promotion_banner":{"experiment_id":"3025397781073","type":"visitor","group":"control","trigger":"finished","log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"app_directory_partner_promotion_banners":{"experiment_id":"3009458145893","type":"visitor","group":"control","trigger":"finished","log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"ca_release_lp":{"experiment_id":"3440535643092","type":"visitor","group":"on","trigger":"launch_visitor","schedule_ts":1653497689,"log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"},"ssb_first_show_team_name":{"experiment_id":"3511918704003","type":"visitor","group":"on","trigger":"finished","log_exposures":false,"exposure_id":"a7c4857ca35f28a94da2f72ec314de60"}},"no_login":false};</script><script type="text/javascript" crossorigin="anonymous" src="https://a.slack-edge.com/bv1-10/primer-vendor.d85d6c1.primer.min.js" onload="window._cdn ? _cdn.ok(this, arguments) : null" onerror="window._cdn ? _cdn.failed(this, arguments) : null"></script><script type="text/javascript" crossorigin="anonymous" src="https://a.slack-edge.com/bv1-10/login-core.44ea278.primer.min.js" onload="window._cdn ? _cdn.ok(this, arguments) : null" onerror="window._cdn ? _cdn.failed(this, arguments) : null"></script><link href="https://a.slack-edge.com/bv1-10/login-core.a0049ff.primer.min.css" rel="stylesheet" type="text/css" onload="window._cdn ? _cdn.ok(this, arguments) : null" onerror="window._cdn ? _cdn.failed(this, arguments) : null" crossorigin="anonymous"><link href="https://a.slack-edge.com/3b81709/style/rollup-slack_kit_base.css" rel="stylesheet" id="slack_kit_helpers" type="text/css" onload="window._cdn ? _cdn.ok(this, arguments) : null" onerror="window._cdn ? _cdn.failed(this, arguments) : null" crossorigin="anonymous"><link href="https://a.slack-edge.com/a8568d7/style/rollup-slack_kit_helpers.css" rel="stylesheet" id="slack_kit_helpers" type="text/css" onload="window._cdn ? _cdn.ok(this, arguments) : null" onerror="window._cdn ? _cdn.failed(this, arguments) : null" crossorigin="anonymous">

<!-- slack-www-hhvm-main-iad-belg/ 2023-01-17 09:48:04/ v3c69136ae030b4bc6d7fe63fd6272a771a534ef8/ B:H -->

</body></html>