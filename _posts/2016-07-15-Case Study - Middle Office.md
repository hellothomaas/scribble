---
layout: post
title: Case Study - Middle Office
date: 2013-05-06 15:27:31
---

## Middle Office

You are a middle office that receives booking information on behalf of your clients.

> Travel agencies use your software to drop new bookings. At some point, they will enter the customers’ payment data in your software. In order to minimize your PCI scope, this payment data should be added without touching your server.

We support different approaches how you can securely collect the customers´ credit card details. Start with a simple HTML `<a href>` tag:

<a href="https://pilot.datatrans.biz/upp/jsp/upStart.jsp?merchantId=1100004624&refno=pci-proxy-redirect&amount=1&currency=CHF&theme=DT2015&uppAliasOnly=yes" target="_blank" class="big-button gray">Collect Credit Card</a>

---

{% highlight html %}
<a href="https://pilot.datatrans.biz/upp/jsp/upStart.jsp
            ?merchantId=1100004624
            &refno=pci-proxy-redirect
            &amount=1
            &currency=CHF
            &theme=DT2015
            &uppAliasOnly=yes">Collect payment data</a>
{% endhighlight %}

PCI Proxy supports a varienty of [different approaches for you to collect the payment data][1]. Your server will never get in touch with sensitive card data which reduces your PCI scope immediately.

 The most common approach is to submit data directly from your software using our [payment pages][2]. Another option is [pay-by-email][3] where temporary payment links are issued that can be emailed to customers to let them enter their payment details by themselves.

 {% highlight ruby %}
 <a href="https://pilot.datatrans.biz/upp/jsp/upStart.jsp
             ?merchantId=1100004624
             &refno=pci-proxy-redirect
             &amount=1
             &currency=CHF
             &theme=DT2015
             &uppAliasOnly=yes">Collect payment data</a>
 {% endhighlight %}

*On behalf of your clients you want to process the booking or transact with different endpoints (e.g. Expedia, Stripe, TUI, Lufthansa, etc.).*

 PCI Proxy allows you to [forward vaulted payment data][4] to PCI compliant third parties.



1. List with code

  ```html
  not highlighted
  multi line
  ```
2. List with code{% highlight javascript %}
var dom = document.getElementById('boom')
console.log(dom);
{% endhighlight %}

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.

{% highlight ruby %}
<a href="https://pilot.datatrans.biz/upp/jsp/upStart.jsp
            ?merchantId=1100004624
            &refno=pci-proxy-redirect
            &amount=1
            &currency=CHF
            &theme=DT2015
            &uppAliasOnly=yes">Collect payment data</a>
{% endhighlight %}

[1]: collect_payment_data.html
[2]: website-application.html
[3]: https://www.datatrans.ch/en/offer/special-solutions/pay-by-e-mail
[4]: forward.html
