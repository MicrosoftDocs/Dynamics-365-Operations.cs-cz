---
title: "Nastavení displeje mobilního zařízení skladu"
description: "Tento článek popisuje, jak nastavit vzhled displeje mobilního zařízení a namapovat klávesové zkratky na ovládací prvky, jako jsou například tlačítka."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4d1e1f953d0088d6d35025136f486f1ad04a9f18
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="warehouse-mobile-device-display-settings"></a>Nastavení displeje mobilního zařízení skladu

[!include[banner](../includes/banner.md)]


Tento článek popisuje, jak nastavit vzhled displeje mobilního zařízení a namapovat klávesové zkratky na ovládací prvky, jako jsou například tlačítka. 

Tento článek se vztahuje k funkcím „pokročilého uskladnění“ v modulu Řízení skladu. Mobilní zařízení lze použít pro řadu úloh, které provádějí pracovníci skladu.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Určení stylů a mapování klávesových zkratek
V rámci konfigurace mobilního zařízení můžete definovat různá rozvržení pro mobilní zařízení. Chcete-li to provést, je nutné znát název souboru Cascading Style Sheets (CSS) a souboru Active Server Page Extension (ASPX). Výchozí soubory jsou nainstalovány v rámci instalace portálu pro mobilní zařízení skladu. Pokud si nejste jisti s názvy souborů, požádejte správce systému. Je možné určit nový styl na stránce **Nastavení displeje mobilního zařízení**:

-    Do pole **Soubor CSS** zadejte název souboru CSS. Včetně přípony souboru .css.
-   V poli **Zobrazení nastavení displeje mobilního zařízení** upřesněte soubor ASPX. **Bez** přípony souboru .aspx.

Soubory CSS a ASPX musí být umístěny v konkrétním adresáři tak, aby je mohla načíst aplikace Internet Information Services (IIS). K definování různých souborů CSS může být užitečné, pokud používáte funkce mobilního zařízení v různých prohlížečích nebo na různých druzích hardwaru vyžadujících jiné ovládací prvek rozvržení. Jednoduchá nastavení, jako je například barva pozadí, písma a velikosti písma pro text, a šířka a funkce tlačítek, lze snadno ovládat pomocí různých souborů CSS. Soubor ASPX je používán k zobrazení mobilního webu v aplikaci na straně serveru ASP.NET. Soubor určuje, jak je rozložena celková struktura HTML. Je vhodné přizpůsobit tuto funkci pouze v případě, že máte vážné strukturální problémy s HTML a jazykem JavaScript, a pro konkrétní zařízení musíte tento kód změnit. Pro mapování ovládacích prvků HTML do klávesových zkratek na stránce mobilního zařízení na stránce **Nastavení displeje mobilního zařízení** v poli **Klávesová zkratka**, přiřaďte pro klávesy číselné kódy. K nalezení kódů číselných znaků v mobilním zařízení lze použít nabídku **Zobrazit kódy pro klávesové zkratky**. Všimněte si, že mapování se mohou lišit v závislosti na hardwaru, který se používá. Pro vytvoření mapování musíte použít následující syntaxi:

&lt;název ovládacího prvku&gt;(&lt;název klávesy&gt;)=&lt;kód klávesy&gt;;

V tomto poli je vysvětlení částí syntaxe:

-   **&lt;název ovládacího prvku&gt;** – název ovládacího prvku (například tlačítka), který je generován v jazyce HTML.
-   **(&lt;název klávesy&gt;)** – název klávesy na klávesnici, pro kterou vytváříte zástupce.
-   **&lt;Kód klávesy&gt;** – kód v podobě číselného znaku klávesy, kterou chcete použít pro klávesovou zkratku.

Následuje příklad:

Storno (Esc) = 27; Úplné (F2) = 113

Na všech stránkách zahrnující tlačítko **Storno**, bude mít tlačítko tento text:

**(Esc) Storno**

Stisknutím klávesy Esc klávesnici aktivujete tlačítko **Storno**. Pro použití nastavení stylu a klávesové zkratky ve specifickém zařízení je nutné vytvořit mapování v poli **Kritéria**. K vytvoření mapování je nutné použít regulární výraz .NET, a výraz musí obsahovat tři části, které jsou odděleny svislou čáru (|), jak je uvedeno zde:

Request.UserHostAddress=&lt;hostitelská adresa uživatele&gt;|HostName=&lt;uživatelské jméno hostitele&gt;|Request.UserAgent=&lt;agent uživatele&gt;

V tomto poli je vysvětlení částí výrazu:

-   **&lt;hostitelská adresa uživatele&gt;** – Regulární výraz .NET shodující se s žadatelem adresy IP.
-   **&lt;uživatelské jméno hostitele&gt;** – Regulární výraz .NET shodující se s žadatelem názvu sítě.
-   **&lt;agent uživatele&gt;** – Regulární výraz .NET shodující se s identifikátorem prohlížeče použitého žadatelem.

Následující příklad umožňuje použití aplikace Internet Explorer 8.

Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0

Lze použít nabídku **Zobrazit konfiguraci serveru pro nastavení displeje** na mobilním zařízení k nalezení informací o nastavení.

## <a name="define-text-colors-for-messages"></a>Definice barvy textu pro zprávy
K nastavení různých barev používaných ve zprávách generovaných systémem, například chybových zprávách, lze použít stránku **Barvy textu mobilního zařízení**. Barva textu může například označovat účel nebo závažnost zprávy. Zobrazeny jsou následující typy zpráv:

| Typ zprávy | Popis                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Výchozí      | Výchozí zprávy používají výchozí nastavení barev pro všechny zprávy, jak je definováno souborem CSS pro portál skladu pro mobilní zařízení.                                                   |
| Chyba        | Chybové zprávy určí problém, který uživatel musí vyřešit předtím, než může pokračovat.                                                                                             |
| Úspěch      | Zprávy s informacemi o úspěšnosti potvrzují, že akce proběhla úspěšně.                                                                                                                                |
| Upozornění      | Upozornění informují pracovníka, že je, nebo by mohlo dojít k problému, pokud bude pracovník pokračovat. Pracovník však nemusí vyřešit problém, aby mohl pokračovat. |

Barvu vyberte na stránce **Vybrat barvu**, klepněte na paletu nebo zadejte hexadecimální barevný kód.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>DEfinujte formát data, který má být použit pro mobilní zařízení
Můžete rozšířit seznam povolených formátů data pro jednotlivé instalace. Tato možnost může být například užitečná, pokud chcete zadat formát, který usnadňuje pracovníkovi zadání data pro mobilní zařízení. Výchozí formát je určen výchozím jazykem uživatele, který je specifikován v poli **Jazyk** na stránce **Možnosti uživatele**. ((Stránka rovněž slouží k přidružení zaměstnance s pracovním uživatelem určitého skladu.).) **Poznámka:** Portál skladu pro mobilní zařízení nepoužívá nastavení pole **Datum, čas a formát čísla** na stránce **Předvolby jazyka a oblasti**. Změna formátu data vyžaduje vaši znalost s regulárními výrazy v rozhraní Microsoft .NET Framework. Další informace naleznete v tématu [Regulární výrazy rozhraní .NET Framework](http://go.microsoft.com/fwlink/?LinkId=391260). Chcete-li definovat formáty data, upravte soubor Dates.ini umístěný v cestě Content\\Settings\\Dates.ini na serveru portálu skladu pro mobilní zařízení. Tento soubor využívá regulární výrazy .NET k určení formátu data. Regulární výraz musí obsahovat dílčí výrazy tvořící pojmenované skupiny pro daný den, měsíc a rok (DDMMRR), jak je uvedeno v následujícím příkladu:

^(?&lt;den&gt;\\d{2})(?&lt;měsíc&gt;\\d{2})(?&lt;rok&gt;\\d{2})$

Každý dílčí výraz vyžaduje jednu nebo dvě číslice pro den a měsíc, a jednu až čtyři číslice pro rok. V následujícím příkladu je dílčí výraz, který definuje pojmenovanou skupinu pro rok, a vyžaduje dvě až čtyři číslice:

(?&lt;rok&gt;\\d{2,4})

Ve stejném souboru můžete zadat více než jeden výraz. Každý výraz musí být na samostatných řádcích. První shodný výraz slouží k analýze data.

<a name="see-also"></a>Viz také
--------

[Konfigurace mobilních zařízení pro práci ve skladu](configure-mobile-devices-warehouse.md)




