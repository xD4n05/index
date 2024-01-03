var ExcelFormulas={DaysBetween:function(date1,date2){var oneDay=24*60*60*1000;return Math.round(Math.abs((date1.getTime()-date2.getTime())/oneDay));},XNPV:function(rate,values){var xnpv=0.0,firstDate=new Date(values[0].Date);for(var key in values){if(values.hasOwnProperty(key)){var tmp=values[key],value=tmp.Flow,date=new Date(tmp.Date);xnpv+=value/Math.pow(1+rate,this.DaysBetween(firstDate,date)/365);}}
return xnpv;},XIRR:function(values,guess){guess=guess||0.1;var x1=0.0,x2=guess,f1=this.XNPV(x1,values),f2=this.XNPV(x2,values),ki;for(ki=0;ki<100;ki++){if((f1*f2)<0.0){break;}
if(Math.abs(f1)<Math.abs(f2)){f1=this.XNPV(x1+=1.6*(x1-x2),values);}
else{f2=this.XNPV(x2+=1.6*(x2-x1),values);}}
if((f1*f2)>0.0){return null;}
var f=this.XNPV(x1,values),rtb,dx;if(f<0.0){rtb=x1;dx=x2-x1;}
else{rtb=x2;dx=x1-x2;}
for(var i=0;i<100;i++){dx*=0.5;var x_mid=rtb+dx,f_mid=this.XNPV(x_mid,values);if(f_mid<=0.0){rtb=x_mid;}
if((Math.abs(f_mid)<1.0e-6)||(Math.abs(dx)<1.0e-6)){return x_mid;}}
return null;}};function doHIntent(){if(isID('trigger_comments')){$("#trigger_comments").hoverIntent({sensitivity:1,interval:100,timeout:0,over:function(){$("#comments_preview").addClass('fadeIn').removeClass('hidden');},out:function(){$("#comments_preview").removeClass('fadeIn').addClass('hidden');}});}
if(isID('pim_carousel')){$('#pim_carousel').find('img').hoverIntent({sensitivity:1,interval:100,timeout:0,over:function(){$('.pim_carousel').find('img').removeClass('selected');$(this).addClass('selected');$('#pm_image').find('.pm_img').removeClass('selected').end().find($(this).attr('data-large')).addClass('selected');},out:function(){}}).on('click',function(){$('#pm_image').find($(this).attr('data-large')).trigger('click');});}
$('.comments_carousel').find('img').hoverIntent({sensitivity:1,interval:100,timeout:0,over:function(){$(this).closest('.comments_carousel').find('.pm_gal').removeClass('selected');$(this).addClass('selected');},out:function(){}});}
function go2comments(){$('#comments_top').on('click',function(){var cd=$('#pe_rating'),cdo=cd.offset(),cdt=0;if(typeof cdo==='object'&&cdo.hasOwnProperty('top')){cdt=cdo.top;}
animatePage(cdt,animationspeed);if(isMobile()){$('#comentarii').trigger('click');}});}
function nlReview(){var lhash=location.hash;if(!empty(lhash)&&lhash==='#review'){var desc=$('#pe_descriere');if(isMobile()){desc.find('.pe_title').trigger('click');}
var mtop=desc.offset();if(typeof mtop==="object"&&mtop.hasOwnProperty('top')){animatePage(mtop.top,animationspeed);}}}
function galleryPrev(){var tc=$('#thumbs_container'),active=tc.find('.selected').parent(),currentIndex=tc.find('a').index(active),prv=tc.find('a').filter(function(index){return index==currentIndex-1;});if(currentIndex>0){prv.trigger('click');}
else{tc.find('a:last-child').trigger('click');}}
function galleryNext(){var tc=$('#thumbs_container'),active=tc.find('.selected').parent(),currentIndex=tc.find('a').index(active),nxt=tc.find('a').filter(function(index){return index===currentIndex+1;});if(active.is(':last-child')){tc.find('a:first').trigger('click');}else{nxt.trigger('click');}}
function galleryImageMobile(){$('body').on('click','.gallery_prev',function(e){e.preventDefault();galleryPrev();e.stopPropagation();}).on('click','.gallery_next',function(e){e.preventDefault();galleryNext();e.stopPropagation();});}
function tcl(){$('.tcl_trigger').on('click',function(e){e.preventDefault();$('#clbox').toggleClass('hidden');});}
function eventTogether(){$('#csdsk_rservice_224281').on('click',function(){if($(this).is(':checked')){$('.ps_addtocart').find('button').attr("onclick","twEvent('Shopping', 'Testare', 'Pagina produs');");}
else{$('.ps_addtocart').find('button').removeAttr("onclick");}});}
function resetCities(){$('#clselc').empty().append("<option value='0'>"+$.i18n._('loading')+"</option>").trigger('chosen:updated');}
function changeLocation(id){$.ajax({url:absolute_store_link+"/ajax/location?id="+id,success:function(msg){if(msg==='1'){window.location.reload();}
else{alert($.i18n._('city_not_found'));}}});}
function changeDistrict(el){var v=parseInt(el.val());if(v===9){resetCities();changeLocation(13818);}
else if(v>0){resetCities();$.ajax({url:absolute_store_link+"/ajax/cities?state="+v+"&hide_not_listed=1",success:function(msg){$('#clselc').html(msg).trigger('chosen:updated');}});}
else{$('#clselc').empty().append("<option value='0'>"+$.i18n._('select_district')+"</option>").trigger('chosen:updated');}}
function changeCity(el){var v=parseInt(el.val());if(v>0){changeLocation(v);}}
function tbiRepopulate(){var v=$('#pscb-rts').find(':selected').val();$('.pscbo-value').each(function(){$(this).text($(this).attr('data-'+v));})}
function payURepopulate(){var v=$('#pscb-rts2').find(':selected').val();$('.pscbo-value2').each(function(){$(this).text($(this).attr('data-'+v));});}
function brdRepopulate(){var v=$('#pscbrd-rts').find(':selected').val();$('.pscbord-value').each(function(){$(this).text($(this).attr('data-'+v));})}
function gameVideo(){$('.pe_grg_top').on('click',function(){$('.pe_gr_game').removeClass('selected');$(this).parent().toggleClass('selected');var tg=$('#pe_games_right').find($(this).attr('data-target')),vid=$(this).attr('data-video');tg.siblings('.pe_gr_game').removeClass('selected').find('.videoWrapper').html('');var dnt=1;if(typeof ckSelection=='object'&&!empty(ckSelection)&&ckSelection.hasOwnProperty('marketing')&&ckSelection['marketing']==1){dnt=0;}
var url=vid+'&byline=0&portrait=0&title=0&speed=0&autopause=0';if(!empty(dnt)){url=url+'&dnt=1';}
tg.addClass('selected').find('.videoWrapper').html('<iframe width="1280" height="720" src="'+url+'" width="1920" height="1080" allowfullscreen></iframe>');});}
function getParamByName(name){var url=window.location.href;url=url.toLowerCase();name=name.replace(/[\[\]]/g,"\\$&").toLowerCase();var regex=new RegExp("[?&]"+name+"(=([^&#]*)|&|#|$)"),results=regex.exec(url);if(!results){return null;}
if(!results[2]){return'';}
return decodeURIComponent(results[2].replace(/\+/g," "));}
function pageGameVideo(){var gid=getParamByName('game_id');if(is_numeric(gid)){var f=$('#pgame_'+gid).find('.pe_grg_top').trigger('click');$('#pe-games').find('.pe-title').trigger('click');}}
function galleryImage(){$('body').on('click','#thumbs_container a',function(e){e.preventDefault();$('#thumbs_container').find('img').removeClass('selected');var ig=$('#gallery_image');if($(this).attr('data-type')==='i'){var oImg=ig.find('img.mfp-img');if(oImg.length>0){oImg.attr('src',$(this).attr('href'));}
else{ig.html('<img src="'+$(this).attr('href')+'" class="mfp-img">');}}
else if($(this).attr('data-type')==='v'){var oIfr=ig.find('iframe');if(oIfr.length>0){oIfr.attr('src',$(this).attr('href'));}
else{ig.html('<div class="responsiveVideo"><iframe src="'+$(this).attr('href')+'" width="640" height="360"></iframe></div>');}}
$(this).find('img').addClass('selected');e.stopPropagation();});$(window).on('keydown',function(e){if(e.which===37||e.which===38){galleryPrev();e.stopPropagation();}
else if(e.which===39||e.which===40){galleryNext();e.stopPropagation();}});}
function swipeGallery(){$('body').livequery(function(){if(isID('gallery_image')){$('#gallery_image').swipe({swipe:function(event,direction){if(direction==='left'){galleryNext();}
else if(direction==='right'){galleryPrev();}},threshold:0});}});}
function gbundlesubmit(){$('.gbundles-submit').on('click',function(){$(this).addClass('button-custom-red');$(this).parent().find('input[type="checkbox"]').prop('checked',true);});}
function syncBox(){$('#product_bottom').find('input[type="checkbox"]').each(function(){$(this).on('change',function(){if($(this).is(':checked')){$('#prodtabs').find('#'+$(this).attr('id').replace("csmob_","csdsk_")).prop('checked',true);}
else{$('#prodtabs').find('#'+$(this).attr('id').replace("csmob_","csdsk_")).prop('checked',false);}});});$('#prodtabs').find('input[type="checkbox"]').each(function(){$(this).on('change',function(){if($(this).is(':checked')){$('#'+$(this).attr('id').replace("csdsk_","csmob_")).prop('checked',true);}
else{$('#'+$(this).attr('id').replace("csdsk_","csmob_")).prop('checked',false);}});});}
function bClick(){$('body').on('change','#csdsk_rservice_'+warranty_servskills_1,function(){$('#csdsk_rservice_'+warranty_servskills_2).prop('checked',false);$('#csmob_rservice_'+warranty_servskills_2).prop('checked',false);}).on('change','#csdsk_rservice_'+warranty_servskills_2,function(){$('#csdsk_rservice_'+warranty_servskills_1).prop('checked',false);$('#csmob_rservice_'+warranty_servskills_1).prop('checked',false);}).on('change','#csmob_rservice_'+warranty_servskills_1,function(){$('#csdsk_rservice_'+warranty_servskills_2).prop('checked',false);$('#csmob_rservice_'+warranty_servskills_2).prop('checked',false);}).on('change','#csmob_rservice_'+warranty_servskills_2,function(){$('#csdsk_rservice_'+warranty_servskills_1).prop('checked',false);$('#csmob_rservice_'+warranty_servskills_1).prop('checked',false);}).on('change','#csdsk_rservice_'+insurance_product_id,function(){$('#csdsk_rservice_'+insurance_product_id).prop('checked',false);$('#csmob_rservice_'+insurance_product_id).prop('checked',false);}).on('change','#csmob_rservice_'+insurance_product_id,function(){$('#csdsk_rservice_'+insurance_product_id).prop('checked',false);$('#csmob_rservice_'+insurance_product_id).prop('checked',false);}).on('click','.set-comment-alert, .set-product-alert',function(){var commentid=$(this).hasClass('set-comment-alert')?$(this).attr('data-comment'):$(this).attr('data-product'),type=$(this).hasClass('set-comment-alert')?'comment':'product';$('#set'+(type==='product'?"product":"")+'alert-'+commentid).text($.i18n._('saving'));$.ajax({url:absolute_store_link+"/ajax/comment_alert?type=set"+(type==='product'?"product":"")+"&id="+commentid,success:function(msg){if(msg==='1'){$('#set'+(type==='product'?"product":"")+'alert-'+commentid).addClass('hidden').text((type==='product'?$.i18n._('alert_new_comment'):$.i18n._('follow_comment')));$('#unset'+(type==='product'?"product":"")+'alert-'+commentid).text((type==='product'?$.i18n._('alert_comment_delete'):$.i18n._('notifications_optout'))).removeClass('hidden');$('#divset-alert-'+commentid).addClass('hidden');}
else{alert($.i18n._('alert_save_error'));}}});}).on('click','.unset-comment-alert, .unset-product-alert',function(){var commentid=$(this).hasClass('unset-comment-alert')?$(this).attr('data-comment'):$(this).attr('data-product'),type=$(this).hasClass('unset-comment-alert')?'comment':'product';$('#unset'+(type=='product'?"product":"")+'alert-'+commentid).text($.i18n._('notifications_optout'));$.ajax({url:absolute_store_link+"/ajax/comment_alert?type=unset"+(type=='product'?"product":"")+"&id="+commentid,success:function(msg){if(msg==1){$('#unset'+(type=='product'?"product":"")+'alert-'+commentid).addClass('hidden').text($.i18n._('notifications_optout'));$('#set'+(type=='product'?"product":"")+'alert-'+commentid).text((type=='product'?$.i18n._('alert_new_comment'):$.i18n._('follow_comment'))).removeClass('hidden');$('#divset-alert-'+commentid).removeClass('hidden');$('#setaproductalert-'+commentid).addClass('seta-product-alert').text($.i18n._('first_comment'));}
else{alert($.i18n._('comment_alert_error'));}}});}).on('dblclick','.set-comment-alert, .set-product-alert, .unset-comment-alert, .unset-product-alert, .set-comment-alert-unregistered, .set-product-alert-unregistered, .seta-product-alert-unregistered',function(){$(this).trigger('click');});}
function toggleUnsealed(){var unsealed=$('#pe_wrap').find('#pe_unsealed'),l=unsealed.find('#unstoggle'),p=l.parent().parent(),pex=unsealed.find('.pe_unsealed_extra'),lhash=location.hash,pt=unsealed.offset(),ptop=0;if(typeof pt==='object'&&pt.hasOwnProperty('top')){ptop=pt.top;}
if(typeof lhash!="undefined"&&/^#u\d+$/.test(lhash)){unsealed.find('.pe_content').show();pex.removeClass('dn');p.removeClass('pe_unsealed_overflow');l.html($.i18n._('show_less_unsealed'));}
l.on('click',function(){pex.toggleClass('dn');p.toggleClass('pe_unsealed_overflow');if(p.hasClass('pe_unsealed_overflow')){if(total_unsealed!==1){$(this).html($.i18n._('show_all_unsealed',total_unsealed));}else{$(this).html($.i18n._('show_one_more_unsealed'));}
$(window).scrollTop(ptop,animationspeed);}
else{$(this).html($.i18n._('show_less_unsealed'));}});}
function fixedp(){var fp=$('#fixed-product'),lto=$('#product_name').offset(),lt=20,ph=fp.outerHeight();if(typeof lto==='object'&&lto.hasOwnProperty('top')){lt=parseInt(lto.top+lt);}
fp.css('top',lt);$(window).on('scroll',function(){var wh=$(window).height();if(parseInt(lt+ph)>wh){fp.css('top',parseInt(wh-ph-10));}});}
function filterComments(){$('#average_rating_container').find('input[type="checkbox"]').on('click',function(){if(typeof $(this).attr('id')!=='undefined'&&$(this).attr('id').substr(0,6)==='rating'){$(this).parent().siblings().children('input[type="checkbox"]').prop('checked',false);}
else{$(this).siblings('input[type="checkbox"]').prop('checked',false);}
if(typeof $(this).attr('data-url')!=='undefined'){window.location=$(this).attr('data-url');}});}
function commentVote(){$('.votes').find('.comment_vote').on('click',function(){var comment=$(this).attr('data-comment'),product=$(this).attr('data-product');if($(this).hasClass('yes')||$(this).hasClass('no')){$.ajax({url:absolute_store_link+'/ajax/votcomentariu/'+product+'/'+comment+'/'+($(this).hasClass('yes')?'da':'nu'),success:function(data){$('#votes-'+comment).html(data);}});return false;}});}
function initGallery(){$('.pm_gal').magnificPopup({type:'ajax',preloader:false,closeMarkup:'<a href="javascript:" class="mfp-close"><span class="mfp_close_sp hidden-mobile">'+$.i18n._('close_escape')+'</span> <span class="mfp_close_btn mfp_close_sp">&times;</span></a>',fixedContentPos:true,fixedBgPos:true,overflowY:'hidden',alignTop:true,closeOnBgClick:false,callbacks:{ajaxContentAdded:function(){$('.scroller').tinyscrollbar();ytnc();}}});}
function openSetPriceAlert(pid){$.magnificPopup.open({preloader:false,items:{src:absolute_store_link+'/alerta-pret/'+pid+'/'},mp_closeMarkupfixedContentPos:true,fixedBgPos:true,alignTop:true,closeOnBgClick:false,closeMarkup:mp_closeMarkup,type:'ajax'});}
function commentsReply(){$('#product_comments').find('.reply_texta').on('click',function(){var p=$(this).parent();if(!p.hasClass('expanded')){p.addClass('expanded');p.next().removeClass('hidden');autosize($('.reply_texta'));}});}
function commentsReplySend(){$('#product_comments').find('.reply_button').on('click',function(){var err=false,p=$(this).parent().parent(),rt=p.prev().find('.reply_texta'),rtv=rt.val(),name=p.find('.reply_name'),nmv=name.val(),email=p.find('.reply_email'),emv=email.val(),cnf=p.find('.confidentialitate'),ra=$(this).parent().next().find('.reply_alert');if(empty(rtv)){rt.addClass('reply_error');err=true;}
else if(rt.hasClass('reply_error')){rt.removeClass('reply_error');}
if(empty(nmv)){name.addClass('reply_error');err=true;}
else if(name.hasClass('reply_error')){name.removeClass('reply_error');}
if(!cnf.is(':checked')&&cnf.length){if(p.find('.confidentialitate-error').length==0){cnf.next().append("<label class='confidentialitate-error reply-error-c'>*Campul acesta este obligatoriu</label>");}}
if(empty(emv)){email.addClass('reply_error');err=true;}
else if(email.hasClass('reply_error')){email.removeClass('reply_error');}
if(err){return false;}
var parent=$(this).attr('data-parent'),posturl=$(this).attr('data-url'),setalert=ra.attr('checked'),commentdata={"customer_name":nmv,"customer_email":emv,"others":rtv,"set_alert":setalert,"parent":parent};if(is_ssl){posturl=posturl.replace(store_link,absolute_store_link);}
$(this).attr({value:$.i18n._('saving'),disabled:'disabled'});rt.attr('disabled','disabled');$(this).siblings('.reply_button_cancel').attr('disabled','disabled').addClass('hidden');$.ajax({url:posturl+'scrie-comentariu/',type:'POST',data:commentdata,success:function(data){p.parent().prev().find('.reply-content-div').append(data);rt.val('').removeAttr('disabled');p.find('.reply_button_cancel').removeAttr('disabled').removeClass('hidden').trigger('click');p.find('.reply_button').removeAttr('disabled').val($.i18n._('send'));},error:function(){alert($.i18n._('comments_error'));p.find('.reply_button_cancel').removeAttr('disabled').removeClass('hidden').trigger('click');p.find('.reply_button').removeAttr('disabled').val($.i18n._('send'));}});return false;});}
function commentsReplyCancel(){$('#product_comments').find('.reply_button_cancel').on('click',function(){var p=$(this).parent().parent();p.addClass('hidden');p.prev().removeClass('expanded');});}
function submitSetPriceAlert(){var pa=$('#price_alert_form');if(pa.valid()){pa.ajaxSubmit({success:function(msg){$('#price_alert_content_inner').html(msg);}});}
return false;}
function submitCommentAlert(){var pa=$('#comment_alert_form');if(pa.valid()){pa.ajaxSubmit({success:function(msg){$('#comment_alert_content').html(msg);}});}
return false;}
function productAlertU(node){}
function addtowg(){var adc=$('#addto_content'),adr=$('#addto_dir'),arr=$('#addto_cbutton_arr');$('#addto_trigger').on({click:function(){adc.toggleClass('hidden');arr.hasClass('fa-angle-down')?arr.removeClass('fa-angle-down').addClass('fa-angle-up'):arr.removeClass('fa-angle-up').addClass('fa-angle-down');}});$(window).on('resize',function(){adc.addClass('hidden');adr.removeClass('fa-angle-double-up').addClass('fa-angle-double-down');arr.removeClass('fa-angle-up').addClass('fa-angle-down');});}
function displayMoreComments(){$('#see_more_comments').on('click',function(e){e.preventDefault();var t=$(this).text(),t1=$.i18n._('show_comments'),t2=$.i18n._('hide_comments'),pc=$('#product_comments');if(t===t1){pc.find('.comments_wishlist.dn').removeClass('dn').addClass('db2');$(this).text(t2);}
else{pc.find('.db2').removeClass('db2').addClass('dn');$(this).text(t1);}
$(this).toggleClass('vz');$('#cmmod').toggleClass('vz');});}
function gbundles(){$('#gbundles_trigger').on('click',function(e){e.preventDefault();$('.gboverflow').toggleClass('vz');$(this).toggleClass('vz');$('#gbmod').toggleClass('vz');toggleText($(this),$.i18n._('hide_bundles'),$.i18n._('display_bundles'));});}
function s1(){$('.psc_bubble').addClass('hidden');$('#psc-bubble').removeClass('hidden');document.getElementById("psc-bubble").style.color='blue';}
function s2(){$('.psc_bubble').addClass('hidden');$('#psc-bubble2').removeClass('hidden');document.getElementById("psc-bubble2").style.color='red';}
function fxAdd(){if(isMobile()){var d=$("#fxaddc");if(typeof navigator!=='undefined'&&typeof navigator.platform!=='undefined'&&/iPad|iPhone|iPod/.test(navigator.platform)){d.addClass('isios');}
var pbOff=$('#product_bottom').offset(),ttop=typeof pbOff==='object'&&pbOff.hasOwnProperty('top')?pbOff.top:0;var vs=viewport_size(),wh=typeof vs==='object'&&vs.hasOwnProperty('height')?vs.height:0;var ppOff=$('#product_price_container').offset(),ptop=typeof ppOff==='object'&&ppOff.hasOwnProperty('top')?ppOff.top:0;if(ttop>0&&wh>0&&ptop>0){$(window).on('scroll',function(){var sT=$(window).scrollTop();(sT<(ptop-wh)||sT>ttop)?d.removeClass('hidden'):d.addClass('hidden');});$('#fxadd').on('click',function(e){e.preventDefault();$('.ps_addtocart').find('button').trigger('click');});}}}
$(document).ready(function(){genericCarousel($('#pim_carousel'));genericCarousel($('#pim_carousel_own'));mobile_accordion($('#product_extra'),false);fScrollbar();bClick();doHIntent();initGallery();galleryImageMobile();galleryImage();swipeGallery();nlReview();tcl();gbundles();if(isID('prodtabs')){tabs($('#prodtabs'));syncBox();}
if(isID('pi_location_container')){accordion($('#product_info').find('#pi_location_container'),true);}
if(isID('pe_gbundle')){mobile_accordion($('#viewproduct-gbundles'));gbundlesubmit();}
if(isID('pe_games_container')){gameVideo();pageGameVideo();}
if(isID('csdsk-rservice-224281')){eventTogether();}
if(isID('pe_unsealed')){toggleUnsealed();}
if(isID('fixed-product')){fixedp();$(window).trigger('scroll').on('resize',function(){$(window).trigger('scroll');fixedp();});}
if(isID('average_rating_container')){filterComments();}
if(isID('product_comments')){commentVote();commentsReply();commentsReplySend();commentsReplyCancel();}
if(isID('comments_top')){go2comments();}
$('.tabnavlink').on('click',function(){$(window).trigger('resize');});addtowg();if(isID('see_more_comments')){displayMoreComments();}
if(isID('fxaddc')){fxAdd();}});