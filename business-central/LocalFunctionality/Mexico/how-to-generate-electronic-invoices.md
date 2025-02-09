---
title: Generate Electronic Invoices [MX]
description: After you post a sales invoice in the Mexican version, you must generate an electronic invoice that will be sent to the customer.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.search.form: 132, 25
ms.date: 06/01/2022
ms.author: edupont

---
# Generate Electronic Invoices in the Mexican Version

In [!INCLUDE[prod_short](../../includes/prod_short.md)], after you post a sales invoice you must generate an electronic invoice that will be sent to the customer. You can also export the electronic invoice as an XML file, which you can save to a specified location.  

The following procedure describes how to generate electronic invoices for sales invoices, but the same steps also apply the following documents:

* Sales credit memos  
* Sales shipments  
* Transfer shipments  
* Service invoices  
* Service credit memos  

## To generate electronic invoices for sales invoices  

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Invoice**, and then choose the related link.  
2. Select the posted invoice.  

    > [!NOTE]
    > If you're canceling the posted document, you must specify a reason for the cancellation in the **CFDI Cancellation Reason** field, and you must specify which document substitutes the canceled document in the **Substitution Document No.** field. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]
3. Choose the **Send Electronic Document** action, and then specify if you want to also request a digital stamp for the document.  

    If you choose **Request Stamp**, the posted invoice will be digitally signed by your PAC, and you can then send the posted invoice afterwards. If you choose **Request Stamp and Send**, the posted invoice is digitally signed and sent in one step.

    An email will be sent to the customer with the electronic invoice attached as an XML file. If you selected the **Send PDF Report** field on the **General Ledger Setup** page, a PDF will be included with the XML file.  

    You can view of the status of the electronic invoice on the **Shipping & Billing** FastTab.
4. Optionally, choose the **Export E-Document as XML** action. Select the location where you want to save the electronic invoice as an XML file.  

To verify the electronic invoice activity, on the **Posted Sales Invoice** page, on the **Invoicing** FastTab, the **Electronic Document Sent** and **No. of E-Document Submissions** fields will be updated.  

> [!NOTE]  
> [!INCLUDE[bp_refimplementation](../../includes/bp_refimplementation.md)]  

## Receive payments

Mexican companies must be able to receive payments in accordance with CFDI Withholdings and Payment Information version 2.0. To receive payment in accordance with CFDI version 2.0, you don't need extra settings because the required data will already have been included for the customer invoices. You can't stamp a payment that is applied to an invoice that doesn't have a stamp.

> [!IMPORTANT]  
> The current version of [!INCLUDE [prod_short](../../includes/prod_short.md)] supports receipt of *customer payment information* in accordance with CFDI version 2.0. However, *withholding receipt* is currently not supported in the default version of [!INCLUDE [prod_short](../../includes/prod_short.md)].  

### To stamp the payment  

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Ledger Entries**, and then choose the related link.  
2. Find a payment that you applied to the electronic invoice, and then select this line.
3. Choose the **Send** action, and then specify if you want to also request a digital stamp for the payment.

## See Also

[Set Up Electronic Invoicing](how-to-set-up-electronic-invoicing.md)  
[Electronic Invoicing](electronic-invoicing.md)  
[Mexico Local Functionality](mexico-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
