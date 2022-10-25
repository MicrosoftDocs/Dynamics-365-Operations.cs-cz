---
title: Pracovní prostor řešení Invoice Capture
description: Tento článek poskytuje informace o pracovním prostoru řešení Invoice Capture.
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
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691135"
---
# <a name="invoice-capture-solution-workspace"></a>Pracovní prostor řešení Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Prohlížeč vedle sebe pro řešení Invoice Capture

Zadávání faktur do systému je obvykle časově náročný proces, který je náchylný k chybám, protože úředníci musí procházet více přílohami a okny, aby shromáždili správné informace. Prohlížeč dokumentů vedle sebe vám pomůže zlepšit vaše zkušenosti při práci s fakturami tím, že celý proces usnadní, zefektivní a zpřesní.

Prohlížeč dokumentů vedle sebe umožňuje uživatelům otevřít původní dokument a fakturu vedle sebe ve stejném okně. Stránka faktury je vyplněna informacemi, které pocházejí z původního dokladu faktury. Prohlížeč vytvoří spojení mezi poli stránky faktury a původním dokladem faktury. Prohlížeč také pomáhá uživatelům najít chyby, které existují na stránce faktury.

### <a name="open-the-side-by-side-viewer"></a>Otevřete prohlížeč vedle sebe

V Microsoft Dynamics 365 Finance můžete otevřít prohlížeč vedle sebe ze seznamu na stránce souhrnu nebo ze stránky se seznamem faktur. Můžete jej také otevřít dvojitým klepnutím (nebo dvojitým kliknutím) na záznam nebo výběrem čísla faktury.

### <a name="using-the-side-by-side-viewer"></a>Používání prohlížeče vedle sebe

#### <a name="manually-review-an-invoice"></a>Ruční kontrola faktury

Doklad faktury, který byl importován, může vyžadovat ruční kontrolu kvůli chybám nebo varováním. V prohlížeči vedle sebe se v záhlaví dokumentu zobrazí stav **Importováno** a aktuální verze bude **Originální verze**.

Chcete-li zahájit kontrolu faktury, vyberte **Spustit kontrolu**. Všechna pole lze upravovat. Pole **Stav** je aktualizováno na **Kontrola** a pole **Současná verze** je aktualizováno na **Upravená verze**.

#### <a name="view-and-work-with-messages"></a>Zobrazení a práce se zprávami

Uživatelé by měli zahájit proces kontroly z podokna zpráv. Chybové zprávy jsou označeny červeným X, varovné zprávy jsou označeny trojúhelníkem a informační zprávy jsou označeny kroužkem. Zprávy související se skóre spolehlivosti lze klasifikovat jako varování nebo chyby v závislosti na prahové hodnotě nastavené konfigurační skupinou. Více informací viz [Skupiny konfigurace řešení Invoice Capture](invoice-capture-config-group.md).

Varovné a chybové zprávy lze ignorovat z podokna zpráv, záhlaví faktury nebo řádků faktury. Poté, co je zpráva ignorována, již se nebude zobrazovat jako chyba nebo varování a ověření faktury neprojde.

- Chcete-li ignorovat zprávy z podokna zpráv, vyberte **Ignorovat**. Chcete-li resetovat zprávu, která byla ignorována, vyberte **Ignorovat** znovu. Typ se pak změní z chyby nebo varování na informace.
- Chcete-li ignorovat zprávy z hlavičky faktury nebo řádku faktury, vyberte **Ignorovat** v poli. Symbol zprávy zmizí. Pokud je zpráva resetována z podokna zpráv, zobrazí se znovu.

U zpráv, které souvisejí s poli záhlaví faktury, když vyberete zprávu v podokně zpráv, kurzor se přesune do odpovídajícího pole v sekci záhlaví.

#### <a name="proofread-and-edit-fields"></a>Zkontrolujte a upravte pole

Pokud je hodnota pole načtena z původní faktury pomocí optického rozpoznávání znaků (OCR), objeví se v poli symbol. Pokud vyberete symbol, prohlížeč dokumentů přiblíží a zvýrazní místo, ze kterého je načtena hodnota pole, aby vám pomohl ověřit data faktury.

Chcete-li obnovit původní zvětšení prohlížeče dokumentů, postupujte podle jednoho z těchto kroků:

- Vyberte stejný symbol, který jste vybrali dříve.
- Zvolte tlačítko v pravém horním rohu prohlížeče dokumentů.

Podle potřeby pole upravte. Úpravy se automaticky uloží, když kurzor opustí pole. Symbol napravo od pole označuje, že pole bylo ručně aktualizováno. Po obnovení stránky bude symbol odstraněn.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>Zkontrolujte fakturu a získejte aktuální zprávy

Když pole upravíte, hodnota pole se aktualizuje, ale nové ověřovací zprávy se nevygenerují. Chcete-li získat aktuální zprávy ověření, vyberte **Kontrola**. Aktualizují se zprávy v podokně zpráv, v záhlaví faktury a na řádcích faktury.

#### <a name="complete-the-review"></a>Dokončete kontrolu

Chcete-li kontrolu dokončit, vyberte **Dokončit kontrolu**. Faktury jsou ověřené. Pokud jsou nalezeny nějaké chyby, stav dokumentu zůstane zachován **Probíhá kontrola** a zobrazí se lišta zpráv. Všechny zprávy v podokně zpráv a v záhlaví a řádcích faktury se automaticky aktualizují, aby poskytovaly informace o příčinách neúspěšného ověření.

Po opravení všech chyb blokování lze kontrolu dokončit. Stav dokumentu je aktualizován na **Zkontrolováno** a pole již nelze upravovat. Kontrolu můžete znovu spustit výběrem **Spustit recenzi**.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Vygenerujte nevyřízenou fakturu dodavatele ve Finance

Chcete-li odeslat doklad faktury do připojeného prostředí Finance, vyberte **Generovat**. Pokud se generování faktury nezdaří, zobrazí se na panelu zpráv chybová zpráva.

#### <a name="void-an-invoice"></a>Anulace faktury

Chcete-li anulovat fakturu, vyberte **Anulovat**. Anulované faktury nelze zkontrolovat a nejsou zobrazeny v seznamu **Faktury vyžadují ruční kontrolu**.

### <a name="validation-logic"></a>Logika ověřování

Některá klíčová pole v prohlížeči vedle sebe neexistují v datech přípravy faktur, ale jsou vyžadována pro generování nevyřízených faktur ve Finance. Tato pole jsou odvozena z kombinace aktuálních fakturačních dat a kmenových dat z Finance.

Pole, která musí být odvozena, jsou **Právnická osoba**, **Účet dodavatele** a **Číslo položky**. Musí být odvozeny v následujícím pořadí. Pokud odvození pole selže, proces se zastaví.

1. **Právnická osoba** – Nejprve se odvodí právnická osoba. Pokud je pro právnickou osobu nalezeno aktivní pravidlo mapování, je právnická osoba odvozena na základě názvu společnosti a adresy společnosti.
2. **Účet dodavatele** – Dále je účet dodavatele odvozen na základě aktivního pravidla mapování a kombinace odvozené právnické osoby a jména a adresy dodavatele.
3. **Číslo položky** – Nakonec je název položky odvozen od fáze přípravy na základě následujících tří typů informací:

    - Konfigurované pravidlo mapování
    - Odvozená právnická osoba
    - Odvozený účet dodavatele

Chcete-li spustit ověření, vyberte **Kontrola** v prohlížeči vedle sebe. V současné době validace provádí následující kontroly:

- **Povinná kontrola** – Tato kontrola ověří povinná pole pro prohlížeč vedle sebe. Uživatelé si mohou vybrat, která pole musí být povinná, na stránce **Nastavení konfigurace**.
- **Skóre spolehlivosti** – Uživatelé mohou nastavit práh varování a práh chyby pro skóre spolehlivosti. Tato kontrola se zaměřuje na skóre spolehlivosti z OCR, které je pod těmito prahovými hodnotami. Na základě výsledku ověření se zobrazí chybové nebo varovné zprávy.
- **Právnická osoba** – Tato kontrola potvrzuje, že právnická osoba je ve Finance. Pokud právnická osoba v prostředí Finance neexistuje, ověření se nezdaří.

Když je prohlížeč vedle sebe použit poprvé a uživatel vybere **Kontrola**, jsou spuštěny procesy odvození a validace. Pokud jsou faktury přesné, proces ověření se spustí, když uživatel vybere **Dokončit kontrolu**. Spustí se také, když uživatel vybere **Vygenerovat fakturu dodavatele**.

Proces odvozování probíhá před procesem ověřování a všechna varování nebo chyby pocházejí z procesu ověřování. Varování a chyby budou zaznamenány do Finance.
