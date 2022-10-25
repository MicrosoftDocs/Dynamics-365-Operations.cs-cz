---
title: Přehled řešení Invoice Capture
description: Tento článek poskytuje informace o řešení Invoice Capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691139"
---
# <a name="invoice-capture-solution"></a>Řešení Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tento článek poskytuje informace o řešení Invoice Capture, které automaticky vytváří faktury dodavatele z digitálních obrázků faktur.

Oddělení závazků (AP) spravuje a zpracovává faktury za přijaté zboží a služby. Účetní závazků ověřuje údaje na fakturách dodavatele z následujících důvodů:

- Aby se předešlo zvýšené námaze, pokud jsou nutné úpravy nebo opravy během uzávěrky období
- Aby se platily faktury dodavateli včas a zabránilo se finanční ztrátě v důsledku chyby nebo podvodu

Optické rozpoznávání znaků (OCR) se v posledních letech široce používá v různých průmyslových odvětvích. Nyní je běžné, že tištěné texty jsou digitalizovány, takže je lze elektronicky upravovat, vyhledávat, kompaktněji ukládat a zobrazovat online. Digitální text lze použít ve strojových procesech, jako jsou kognitivní výpočty, strojový překlad, převod textu na řeč, klíčová data a dolování textu.

Evoluce technologie umělé inteligence (AI) umožnila moderním řešením OCR číst různé formáty faktur od různých dodavatelů, aniž by vyžadovaly velký lidský zásah. Stále více společností si uvědomuje, že mohou ušetřit úsilí a zlepšit přesnost tím, že budou faktury zpracovávat automatizací místo ručního zpracování.

## <a name="system-landscape"></a>Přehled systému

Následující obrázek ukazuje hlavní součásti a kroky v řešení Invoice Capture.

[![Komponenty a kroky v řešení Invoice Capture.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Požadované role

V následující tabulce jsou uvedeny role, které jsou nutné k nastavení a používání řešení Invoice Capture.

| Role          | Akce | Systémy | Názvy rolí |
|---------------|---------|---------|-----------|
| Správce | <ul><li>Nastavení prostředí v Microsoft Power Platform.</li><li>Nasazení řešení v Microsoft Power Platform.</li><li>Nastavte připojení mezi Dynamics 365 a AI Builder.</li><li>Nastavit umístění Azure Data Lake Storage.</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Správce Dynamics 365</li><li>Správce Power Platform</li><li>Vlastník dat Blob Storage</li></ul> |
| Tvůrce AI      | <ul><li>Udržujte toky.</li><li>Vytvářejte vlastní modely AI.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Občanští tvůrci</li></ul> |
| Referent závazků      | <ul><li>Zkontrolujte a proveďte akce v oblasti přípravy faktur dodavatele.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Nová role referenta závazků v Power Platform</li></ul> |
| Referent závazků      | <ul><li>Provádějte každodenní operace jako referent závazků.</li><li>Přejděte do pracovní oblasti faktury dodavatele.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Úředník závazků</li></ul> |
  
Další informace o instalaci Invoice Capture viz [Instalace Invoice Capture](../accounts-payable/install-invoice-capture.md).  
