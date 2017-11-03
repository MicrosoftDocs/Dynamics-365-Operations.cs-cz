---
title: "Nastavení kreditu a inkas"
description: "Tento článek popisuje postup nastavení funkce inkasa."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09296ae02c690fa683d853cc91a5abf243bcafa7
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-credit-and-collections"></a>Nastavení kreditu a inkas

[!include[banner](../includes/banner.md)]


Tento článek popisuje postup nastavení funkce inkasa.

<a name="set-up-aging-period-definitions"></a>Nastavit definice období pro sledování splatnosti
-------------------------------

Nastavte definici období pro sledování splatnosti. Definice období pro sledování splatnosti určuje sloupce, které se zobrazují na stránkách se seznamem **Splatné zůstatky**, **Inkasní aktivity** a **Případy inkasa**. Také definuje období, které se zobrazuje na stránce **Inkasa**. Pokud je nastaven fond zákazníků, je použita jeho definice období pro sledování splatnosti. Pokud nejsou nastaveny žádné fondy, použije se výchozí definice období pro sledování splatnosti, která je určena na stránce **Parametry pohledávek**. Pokud není určena žádná výchozí definice období pro sledování splatnosti, použije se první definice období pro sledování splatnosti na stránce **Definice období pro sledování splatnosti**.

## <a name="create-an-aging-snapshot"></a>Vytvoření snímku sledování splatnosti
Vytvořte záznamy snímků sledování splatnosti pro všechny odběratele nebo pro odběratele ve fondu zákazníků. Informace o snímku sledování splatnosti se zobrazují na stránce se seznamem **Splatné zůstatky** a na stránce **Inkasa**. Je třeba snímek sledování splatnosti vytvořit před použitím stránky seznamu. Na stránce se seznamem se zobrazují informace pouze pro odběratele, pro které byl vytvořen snímek sledování splatnosti.

## <a name="optional-set-up-customer-pools"></a>Nepovinné: Nastavení fondů zákazníků
Můžete nastavit fondy zákazníků představující skupiny odběratelů. Fondy zákazníků můžete použít jako filtry pro informace o odběratelích, které se zobrazují na stránkách se seznamem **Inkasa**, na stránce **Inkasa** nebo při vytváření snímků sledování splatnosti.

## <a name="optional-create-a-collections-team"></a>Nepovinné: Vytvoření týmu inkasa
Pokud ve vaší organizaci inkasní práci vykonává více uživatelů, můžete nastavit tým inkasa. Na stránce **Parametry pohledávek** můžete vybrat tým. Pokud nevytvoříte tým inkasa, bude tým vytvořen automaticky při nastavení inkasních agentů na stránce **Inkasní agent**.

## <a name="set-up-a-collections-case-category"></a>Nastavení kategorie případů inkasa
Pokud budete používat případy k organizaci inkasní práce, nastavte kategorii případu, která má typ kategorie **Inkasa**. Toto nastavení je nutné pouze v případě, že chcete použít funkci případu na stránce **Inkasa**.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Nastavení názvů deníků (vyrovnání, odpisu a NFP)
Nastavte názvy deníků používaných při zpracování transakcí na stránce **Inkasa**. Toto zpracování zahrnuje vyrovnání transakce, odpis transakce nebo zpracování platby NFP (nedostatečné finanční prostředky).

| Popis | Typ deníku     |
|-------------|------------------|
| Vyrovnání  | Platba odběratele |
| Odpis   | Denně            |
| NFS         | Platba odběratele |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Nastavení kódu důvodu pro transakce odpisu
Nastavte výchozí kód důvodu, který se použije při odepsání transakcí na stránce **Inkasa**. Během procesu odpisu lze kód změnit.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>Nastavení složky pro přílohy e-mailu a vytváření šablon e-mailů
Pokud budete na stránce **Inkasa** odesílat e-mailové zprávy s přílohami pro aplikaci Microsoft Excel, můžete vytvořit volitelnou e-mailovou šablonu pro ty zprávy.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Nastavení parametrů pohledávek pro inkaso
Nastavte parametry pohledávek, které se zobrazují na kartě **Inkasa**.

## <a name="optional-set-up-collections-agents"></a>Nepovinné: Nastavení inkasních agentů
Pokud ve vaší organizaci inkasní práci vykonává více uživatelů, můžete nastavit inkasní agenty. Inkasní agent je pracovník, který je nastaven jako uživatel na stránce **Vztahy uživatele**. Přiřazením fondů zákazníků (dotazů na odběratele) můžete inkasním agentům usnadnit organizaci jejich práce. Inkasní agenti jsou přidáni do týmu, který je vybrán na stránce **Parametry pohledávek**. Pokud není na této stránce vybrán tým, automaticky se vytvoří nový tým s názvem **Inkasa** a inkasní agenti budou přidáni do tohoto týmu.

## <a name="set-up-a-writeoff-account"></a>Nastavit účtu pro odpis
Nastavte účet pro odpis používaný pro položky odpisu hlavní knihy, když je odepsána transakce. Tento účet je uložen v účetním profilu odběratele.

## <a name="set-up-nsf-information-for-bank-accounts"></a>Nastavení informací NFP pro bankovní účty
Aktualizujte bankovní účty, aby měly správný deník, když jsou na stránce **Inkasa** identifikovány platby NFP. Na kartě **Správa měn** vyberte v poli **Deník plateb NFP** deník plateb.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Nastavení aplikace Outlook pro uživatele stránky Inkasa
Dříve, než budou moci pracovníci na stránce **Inkasa** vytvářet aktivity či odesílat e-mailové zprávy, je nutné ověřit, že je zvolen konfigurační klíč **Synchronizace aplikace Microsoft Outlook** a že je pro tyto pracovníky nastavena synchronizace s aplikací Outlook.

## <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>Nastavení e-mailů a adres pro kontakty inkasa odběratelů
Pokud chcete na stránce **Inkasa** posílat e-mailové zprávy kontaktům odběratelů, nastavte e-mailové adresy těchto kontaktů. Kontaktní osoba pro inkaso se na stránce **Inkasa** používá jako výchozí kontakt. Můžete nastavit adresu pro výpis odběratele, pokud mají mít výpisy adresu odlišnou od primární adresy. 

Na pevné záložce **Úvěry a inkasa** pro odběratele vyberte v poli **Kontakt inkas** osobu z organizace odběratele, která pracuje s vašim inkasním agentem. Tato osoba slouží jako výchozí kontakt na stránce **Inkasa**, kterému jsou odesílány e-mailové zprávy. 

> [!NOTE] 
> Pokud kontaktní osoba inkasa není pro odběratele zadána, použije se primární kontakt odběratele. Pokud není specifikován primární kontakt, e-mailové zprávy budou odeslány na první adresu uvedenou na stránce **Kontakty**.

## <a name="set-up-email-settings-for-salespeople"></a>Nastavení e-mailu pro prodejce
Pokud chcete na stránce **Inkasa** posílat těmto prodejcům e-mailové zprávy, nastavte e-mailové adresy prodejců. Nastavte e-mailovou adresu pro každého obchodního zástupce v každé skupině provizního prodeje. Obchodní zástupce, který má zvolenu možnost **Kontakt**, je výchozí prodejce, kterému jsou odesílány e-mailové zprávy. 

Pokud obchodní zástupce není zadán, použije se primární prodejce pro organizaci odběratele. Pokud není určen primární prodejce, e-mailové zprávy budou odeslány prvnímu prodejci uvedenému na stránce.


Další informace naleznete v následujících tématech:

 - [Vytvoření posloupnosti upomínek](tasks/create-collection-letter-sequence.md)
 
 - [Zpracování upomínek](tasks/process-collection-letters.md)
 
 - [Kontrola inkasních informací](tasks/review-collections-information.md)


