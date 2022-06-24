---
title: Řízení náborových procesů
description: Tento článek popisuje koncept, který mohou náboráři použít ke sledování kroků v procesu náboru.
author: twheeloc
ms.date: 01/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ada6dfc9b227c7ae4ca873e8354d1fcc11ecbaf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910312"
---
# <a name="manage-recruiting-processes"></a>Řízení náborových procesů

> [!IMPORTANT]
> Funkce náboru v tomto článku se bude označovat jako náborové projekty a zaměří se na žadatele, žádosti a náborové projekty. 


Tento článek popisuje koncept, který náboráři mohou použít pro sledování kroků v procesu náboru, včetně úsilí inzerovat otevřené pozice a provádět nábor uchazečů, sledovat informace v přihlášce a o uchazeči, vést pohovor s uchazeči a vybírat jednoho nebo více uchazečů pro naplnění otevřené pozice ve vaší organizaci.

## <a name="overview"></a>Přehled

Náborové projekty vám mohou pomoci uspořádat kroky, které budete provádět při vyplňování otevřených pozic v právnické osobě. Uchazeč je osoba, která se uchází o zaměstnání ve vaší společnosti. Přihláška je vyjádření zájmu uchazeče o zaměstnání ve vaší společnosti a může být vázána na náborový projekt k vyjádření zájmu o konkrétní pozici. Jeden uchazeč může mít více přihlášek v rámci stejné právnické osoby nebo v rámci více společností ve vaší organizaci.

## <a name="recruitment-projects"></a>Náborové projekty

Náborové projekty umožňují náborářům a sledovat pokrok při obsazování jednoho nebo více pracovních míst. Náborový projekt identifikuje oddělení a práci, pro které je otevřena jedna nebo více pozic. Náborové projekty sledují také následující informace pro otevřené pozice:

- Specifický počet otevřených pozic
- Personální konzultant a alternativní kontakt pro pozici
- Datum schválení žádosti
- Konečný termín přihlášky
- Odhadované počáteční datum

Náborový projekt obsahuje hodnotu **Pracovní inzerát** použitý na stránce **Samoobsluha pro zaměstnance** pro inzerování otevřené pozice. Otevřenou pozici lze zaměstnancům zobrazit, pouze když má náborový projekt hodnotu **Pracovní inzerát**, pole **Zobrazit v samoobsluze** pro zaměstnance je nastaveno na hodnotu **Ano**, pole **Konečný termín přihlášky** je nastaven na budoucí datum a náborový projekt musí má hodnotu **Stav projektu** **Zahájeno**. V následující tabulce jsou uvedeny možné stavy náborového projektu a jejich popis.

| Stav    | Udává, že...                                                                         |
|-----------|-----------------------------------------------------------------------------------------|
| Plánováno | Připravuje se úsilí pro nábor. Nábor pro tento projekt ještě nebyl zahájen |
| Zahájeno   | Žádosti jsou nyní přijímány pro volná místa v projektu.                   |
| Dokončeno  | Všechna volná místa pro tento projekt byla naplněna.                                         |
| Stornováno  | Nábor pro tento projekt byl zrušen.                                          |

Náboráři mohou zaznamenávat také **Média** použitá pro reklamu volné pozice skrze externí kanály a sledovat **Vývoj** s ohledem na projekt nebo žádost.

## <a name="applicants"></a>Uchazeči

Uchazeč je osoba, která se uchází o práci ve vaší společnosti. Žadatelé jsou sdíleni všemi právnickými osobami ve vaší organizaci. Proto máte velkou zásobu talentů, ve kterých můžete hledat. Můžete spravovat odkazy, kompetence, požadavky a osobní údaje pro uchazeče. Při vytvoření záznamu žadatele se vytvoří osobní záznam tohoto uchazeče v globálním adresáři. Pomocí stránky **Uchazeč** můžete provádět aktualizace následujících informací pro globální adresář pro osoby, které jsou uchazeči:

- Informace adresy
- Kontaktní informace
- Identifikační informace
- Podrobnosti o jméně
- Osobní údaje

## <a name="applications"></a>Aplikace

Na stránce **Přihláška** můžete zaznamenat údaje z přijatých žádosti o zaměstnání. Přihláška je vyjádření zájmu uchazeče o práci, kterou vaše organizace nabízí. Při vytváření žádosti musí uchazeč již existovat jako uchazeč nebo osoba ve vašem systému.

Žádosti o zaměstnání odeslané uchazeči prostřednictvím webu jsou buď vyžádané žádosti, které byly zadány v reakci na pracovní inzerát, nebo nevyžádané žádosti. Vyžádané žádosti jsou automaticky přiřazeny k náborovému projektu, na jehož základě byl vytvořen daný pracovní inzerát. Nevyžádané žádosti jsou přiřazeny k náborovému projektu, který je určen v oblasti **Nábor** na stránce **Parametry lidských zdrojů**.

### <a name="application-status"></a>Stav přihlášky

Stav přihlášky označuje, kde se přihláška nachází v procesu náboru. V následující tabulce jsou uvedeny možné stavy přihlášky a jejich popis.

| Stav    | Udává, že...                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Přijato  | Datum, kdy byla přihláška přijata.                                                             |
| Potvrzeno | Uchazečům mohou být odeslána potvrzení o příjmu žádosti.            |
| Pohovor | Pozvánka k pohovoru může být odeslána uchazeči.                                     |
| Zamítnutí | Uchazeči může být odesláno zamítavé vyjádření.                                          |
| Stornováno  | Uchazeči může být odesláno potvrzení odstoupení. Tento status se přiřazuje ručně. |
| Zaměstnán  | Uchazeči může být odeslána nabídka k zaměstnání.                                         |

### <a name="correspondence-actions"></a>Akce korespondence

Korespondenční akce Přihlášky určuje šablonu e-mailu nebo dokumentu, která se použije ke komunikaci s uchazečem, který podal přihlášku. Můžete přidružit **záložky přihlášek** ke korespondenčním akcím, což vám umožní použít hodnoty ze stránek **Přihláška**, **Žadatel**, **Pohovor** a **Náborový projekt** při komunikaci s uchazeči. Vytvořením **šablon e-mailu aplikace** lze vytvářet pro akce korespondence k rychlému odeslání e-mailů uchazečům, jejichž přihláška má určitou kombinaci stavu akce a korespondence. Můžete například odeslat e-mail s potvrzením všem uchazečům s hodnotou **Stav** **Přijato** a hodnotou **Akce korespondence** **Přijato**. Po odeslání e-mailu máte možnost automaticky aktualizovat stav žádostí.

## <a name="application-routing"></a>Směrování přihlášek

Má-li přihlášku zkontrolovat několik pracovníků, lze pro vytvoření seznamu střídání zaměstnanců pro řízení procesu použít stránku **Směrování přihlášek**.

## <a name="interviews"></a>Pohovory

**Pohovory s uchazeči** lze naplánovat ze stránky **Žádosti**. Pomocí tlačítka **Odeslat informace o schůzce** odešlete soubor kalendáře s informacemi o plánu interview uchazeči a tazateli.

## <a name="skill-mapping"></a>Mapování dovednosti

**Mapování dovedností** a **Profily mapování dovedností** slouží k identifikaci uchazečů, kteří mohou být vhodní pro volnou pozici.

## <a name="hiring-applicants"></a>Přijímání uchazečů

Pomocí stránky **Přihlášky** můžete najmou uchazeče. Při náboru žadatele bude mít záznam přihlášky stav **Zaměstnán** a osobní záznam uchazeče v globálním adresáři je přidružen k novému záznamu pracovníka. Změny informací v globálním adresáři pro nový záznam pracovníka je zobrazen také v záznamu žadatele. To vám může pomoci snížit objem zadávaní dat, pokud nový pracovník někdy zažádá o jinou pozici v rámci vaší organizace. Pokud chcete přijmout stávajícího pracovníka na novou pozici, klikněte na **Změnit pozici** v rozevíracím seznamu **Stav přihlášky** pro zahájení procesu převodu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
