---
title: Osvědčení o původu USMCA
description: Tato funkce umožňuje vytisknout osvědčení o původu dokumentů vyžadovaných dohodou USA - Mexiko - Kanada (USMCA).
author: Henrikan
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 4d34c1778802baaa0de0506d3dd4bc7efeb13f27
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573050"
---
# <a name="usmca-certification-of-origin"></a>Osvědčení o původu USMCA

[!include [banner](../includes/banner.md)]

Tato funkce umožňuje vytisknout osvědčení o původu dokumentů vyžadovaných dohodou USA - Mexiko - Kanada (USMCA).

*Dokument osvědčení o původu USMCA* obsahuje minimální datové prvky požadované pro deklaraci. Některé datové prvky lze před tiskem předvyplnit, zatímco jiné je nutné po tisku vyplnit ručně. Pro získání preferenčního zpracování cel musí být dokument v době podání prohlášení vyplněn a vlastněn dovozcem. Dokument může vyplnit dovozce, vývozce nebo výrobce.

Dokument můžete vytisknout pro jednu zásilku ze stránky seznamu **Všechny zásilky** nebo ze stránky **Podrobnosti o dodávce**.

Dokument je přístupný, pouze pokud je zemí na primární adrese právnické osoby USA.

V závislosti na výběru tisku dokumentu lze dokument předvyplnit údaji z vašeho systému. Je možné změnit nebo přidat data do tištěného dokumentu exportem tištěného dokumentu do upravitelného formátu, například Microsoft Word. Po exportu můžete použít všechny požadované změny před provedením deklarace.

## <a name="turn-on-the-usmca-feature"></a>Zapnutí funkce USMCA

Než můžete použít funkci USMCA, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Správa přepravy*
- **Název funkce:** *Dokument osvědčení o původu USMCA*

## <a name="document-content"></a>Obsah dokumentu

Dokument osvědčení o původu USMCA obsahuje následující datové prvky:

- Prvky adresy
- Úloha certifikační strany
- Jedna zásilka
- Faktury
- Certifikační období
- Podrobnosti zboží
- Podpis certifikátora
- Počet stránek

Další informace o každém z těchto prvků a o tom, jak se jejich hodnoty nacházejí, najdete ve zbývajících částech tohoto tématu.

## <a name="print-a-usmca-certification-of-origin-document"></a>Tisk dokumentu osvědčení o původu USMCA

Chcete-li u zásilky vytisknout dokument osvědčení o původu USMCA, postupujte takto:

1. Proveďte některou z následujících akcí:
    - Přejděte na **Správa přepravy > Zásilky > Všechny zásilky** a vyberte zásilku, pro kterou chcete dokument vytisknout.
    - Otevřete stránku **Podrobnosti o zásilce** pro zásilku, pro kterou chcete dokument vytisknout (sem se můžete dostat několika způsoby, včetně stránky **Všechny zásilky**).
1. V podokně akcí otevřete kartu **Zásilky** a ve skupině **Tisk** vyberte **Osvědčení o původu USMCA**.
1. Otevře se dialogové okno **Osvědčení o původu**. Proveďte nastavení popsaná v následujících podsekcích a poté vyberte **OK** pro vygenerování dokumentu.
1. Otevře se náhled dokumentu. Pomocí příkazů uvedených v podokně akcí můžete dokument podle potřeby vytisknout nebo exportovat.

### <a name="certifying-party"></a>Certifikační strana

Použijte rozevírací seznam **Certifikační strana** k identifikaci typu strany, která dokument tiskne. Uveďte, zda je certifikační stranou *Vývozce*, *Vývozce a výrobce*, *Výrobce* nebo *Dovozce*; nebo ponechte prázdné, pokud certifikační strana není žádnou z nich. Možnost, kterou vyberete, určuje, co se vytiskne v částech adresy v dokumentu.

**Certifikační strana**, kterou vyberete, bude uvedena v tištěném dokumentu.

Dokument lze vytisknout pro příchozí i odchozí zásilky. Jako *Dovozce* vyberte **Certifikační stranu** pouze pro příchozí zásilky.

Následující tabulka popisuje typy informací, které jsou obsaženy v dokumentu na základě **Certifikační strany**, kterou vyberete.

| Certifikační&nbsp;strana | popis |
|---|---|
| *\[Bianko\]* | Přidá do dokumentu následující podrobnosti:<ul><li>**Podrobnosti o certifikátorovi**: Použije podrobnosti adresy pro přepravní sklad, pokud jsou k dispozici; jinak použije adresu místa dodání, pokud je k dispozici; jinak použije adresu právnické osoby (společnosti) vybrané v Supply Chain Management.</li><li>**Podrobnosti o vývozci**: Prázdné</li><li>**Podrobnosti o výrobci**: Prázdné</li><li>**Podrobnosti o dovozci**: Prázdné</li><ul>|
| *Vývozce* | Přidá do dokumentu následující podrobnosti:<ul><li>**Podrobnosti o certifikátorovi**: Použije podrobnosti adresy pro přepravní sklad, pokud jsou k dispozici; jinak použije adresu místa dodání, pokud je k dispozici; jinak použije adresu právnické osoby (společnosti) vybrané v Supply Chain Management.</li><li>**Podrobnosti o vývozci**: Použije podrobnosti adresy pro právnickou osobu.</li><li>**Podrobnosti o výrobci**: Prázdné</li><li>**Podrobnosti o dovozci**: Použije účet faktury pro související prodejní objednávku.</li><ul>|
| *Vývozce a výrobce* | Přidá do dokumentu následující podrobnosti:<ul><li>**Podrobnosti o certifikátorovi**: Použije podrobnosti adresy pro přepravní sklad, pokud jsou k dispozici; jinak použije adresu místa dodání, pokud je k dispozici; jinak použije adresu právnické osoby (společnosti) vybrané v Supply Chain Management.</li><li>**Podrobnosti o vývozci**: Použije podrobnosti adresy pro právnickou osobu.</li><li>**Podrobnosti o výrobci**: Použije podrobnosti adresy pro právnickou osobu.</li><li>**Podrobnosti o dovozci**: Použije účet faktury pro související prodejní objednávku.</li><ul>|
| *Dovozce* | Přidá do dokumentu následující podrobnosti:<ul><li>**Podrobnosti o certifikátorovi**: Použije podrobnosti adresy pro přepravní sklad, pokud jsou k dispozici; jinak použije adresu místa dodání, pokud je k dispozici; jinak použije adresu právnické osoby (společnosti) vybrané v Supply Chain Management.</li><li>**Podrobnosti o vývozci**: Prázdné</li><li>**Podrobnosti o výrobci**: Prázdné</li><li>**Podrobnosti o dovozci**: Použije podrobnosti adresy pro právnickou osobu.</li><ul>|
| *Výrobce* | Přidá do dokumentu následující podrobnosti:<ul><li>**Podrobnosti o certifikátorovi**: Použije podrobnosti adresy pro přepravní sklad, pokud jsou k dispozici; jinak použije adresu místa dodání, pokud je k dispozici; jinak použije adresu právnické osoby vybrané v Supply Chain Management.</li><li>**Podrobnosti o vývozci**: Prázdné</li><li>**Podrobnosti o výrobci**: Použije podrobnosti adresy pro právnickou osobu.</li><li>**Podrobnosti o dovozci**: Prázdné</li><ul>|

### <a name="has-various-producers"></a>Má různé výrobce

Rozevírací seznam **Certifikační strana** řídí text, který se má použít pro podrobnosti výrobce v dokumentu. Vyberte jednu z následujících možností:

- *Různí výrobci* - Vytiskne text „Různé“ v podrobnostech výrobce.
- *K dispozici na vyžádání* - Vytiskne text „K dispozici na žádost dovozních orgánů“ v podrobnostech výrobce.

Když je **Certifikační strana** nastavena na *Vývozce a výrobce* nebo *Výrobce*, pak se zruší nastavení **Má různé výrobce** a podrobnosti o adrese výrobce budou stejné jako u certifikátora.

### <a name="blanket-period"></a>Certifikační období

Použijte nastavení **Paušální období od** a **Paušální období do** pro stanovení paušální doby, během níž bude dokument pokrývat více zásilek stejného zboží, přestože je dokument vytištěn pouze pro jednu zásilku. Můžete nastavit paušální data období bez jakýchkoli omezení a budou přidána do dokumentu. Můžete také nechat tato nastavení prázdná nebo je nastavit v minulosti.

### <a name="is-single-shipment"></a>Jedná se o jednu zásilku

V dialogovém okně **Osvědčení o původu** nastavte **Jedná se o jednu zásilku** na jednu z následujících možností:

- *Ano* - Přidá „Jedna zásilka: Ano“ vedle čísla faktury.
- *Ne* - Nic nepřidává.

## <a name="other-information-included-in-the-document"></a>Další informace obsažené v dokumentu

Kromě volitelných prvků, které vyberete pomocí dialogového okna **Osvědčení nebo původ** bude dokument Osvědčení o původu USMCA obsahovat informace a vlastní pole shrnutá v následujících podsekcích. Některé z těchto informací je nutné po vygenerování dokumentu zadat ručně.

### <a name="invoice-number"></a>Číslo faktury

ID prodejních faktur vztahujících se k zásilkám jsou vytištěny na dokladu bez ohledu na paušální období. Čísla faktur jsou vytištěna bez ohledu na vobu **Jedná se o jednu zásilku**.

### <a name="item-details"></a>Podrobnosti zboží

Dokument obsahuje několik oddílů, které obsahují seznam konkrétních podrobností položek, kterými jsou:

- **Číslo SKU**: Vytiskne číslo položky uvolněného produktu.

- **Popis**: Vytiskne popis nebo název uvolněného produktu. Pokud existuje popis v jazyce uživatele, vytiskne se. Pokud takový popis neexistuje, vytiskne se název v jazyce uživatele. Pokud tento název neexistuje, vytiskne se název položky.

- **Klasifikace cel harmonizovaného systému (HS)**: Vytiskne plán harmonizovaných cel spojený s produktem. Tyto plány můžete nastavit na adrese **Správa přepravy \> Nastavení \> Přepravní standard \> Plán harmonizovaných cel**.

- **Kritérium původu:** Při prvním vydání dokumentu musíte ručně zadat data do této části.

- **Země původu:** Vytiskne zemi původu, kterou použijete přechodem na **Správa informací o produktu \> Nastavit \> Soulad výrobků \> Země původu** (viz také [Země původu](../pim/country-of-origin.md)). Kód ISO pro zemi původu se vytiskne na základě země / regionu určení v adrese pro doručení zásilky a zboží. Pokud nebyla nastavena žádná data země původu, vrátí se tato hodnota zpět k nastavení nalezenému v **Uvolněný produkt \> Zahraniční obchod \> Původ**. Pokud stále nejsou nalezena žádná data o zemi původu, musíte po vygenerování dokumentu zemi původu zadat ručně.

### <a name="certifier-signature-and-date"></a>Podpis a datum certifikátora

Po vygenerování dokumentu to musíte zadat ručně.

### <a name="consists-of-number-of-pages"></a>Skládá se z počtu stránek

Uživatel podepisující certifikaci musí po vygenerování dokumentu ručně zadat počet stránek (pro ověření).

### <a name="page-numbers"></a>Čísla stránek

Aktuální stránka a počet stránek vytištěných ve spodní části dokumentu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]