---
title: "Nastavení možností zpracování objednávky"
description: "Toto téma poskytuje informace o zpracování objednávek pro kontaktní střediska pomocí aplikace Microsoft Dynamics 365 for Operations - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 52b56274c8b72c67bc0a50f23114cebc510f1667
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-order-processing-options"></a>Nastavení možností zpracování objednávky

[!include[banner](includes/banner.md)]


Toto téma poskytuje informace o zpracování objednávek pro kontaktní střediska pomocí aplikace Microsoft Dynamics 365 for Operations - Retail. 

Maloobchodní a velkoobchodní prodej v aplikaci Microsoft Dynamics 365 for Operations podporuje více maloobchodních sítí, například online obchody, kamenné obchody a kontaktní střediska. V kontaktních střediscích pracovníci zpracovávají zakázky odběratele telefonicky a vytvářejí prodejní objednávky. Toto téma popisuje způsob vytvoření kontaktního střediska a konfigurace možností kontaktního střediska. Každé kontaktní středisko může mít vlastní uživatele, platební metody, cenové skupiny, finanční dimenze a způsoby dodání. Tyto možnosti lze nakonfigurovat při vytváření kontaktního střediska. **Upozornění:** Předtím, než bude možné použít workflow kontaktního střediska, když aktuální uživatel aplikace Dynamics AX vytvoří prodejní objednávky, musí být uživatel přiřazen ke kontaktnímu středisku jako uživatel kontaktního střediska. Můžete využít stránku **Kontaktní středisko** pro povolení nebo zakázání skupin funkcí, které jsou jedinečné pro kontaktní střediska. Lze povolit následující skupiny funkcí:

-   **Dokončení objednávky** – tato skupina obsahuje funkce, které se vztahují k platbám a dokončení objednávek na stránce **Prodejní objednávka**.
-   **Směrovaný prodej** – tato skupina obsahuje funkce, které souvisejí se zdrojovými kódy, skripty a požadavky na katalog.

Pokud povolíte tyto funkce v nastavení kontaktního střediska, budou k dispozici na stránce **Prodejní objednávka** pro uživatele, kteří jsou přiřazeny ke kontaktnímu středisku. Většina těchto funkcí vyžaduje před použitím další konfiguraci. Obrázky a skripty jsou povoleny v rámci řízeného nastavení prodeje pro zvláštní kontaktní středisko. Jsou-li tyto funkce povoleny, skripty a obrázky produktů jsou zobrazeny v části okna s fakty na stránce **Prodejní objednávka**. Zobrazí se výchozí obrázek, který je nastaven pro produkt. Skripty lze konfigurovat pro zboží, katalog, odběratele nebo položky v kontextu katalogu. Objednávky kontaktního střediska mohou zobrazit další podrobnosti o odvození ceny pro konkrétní objednávku. Například objednávky zobrazují slevu, která byla použita. Tuto funkci v povolíte v možnosti **Pohledávky** &gt; **Nastavení** &gt; **Parametry pohledávek** &gt; **Ceny** &gt; **Podrobnosti o ceně**. Lze použít stránku **Podrobnosti o ceně** z rozevíracího seznamu **Řádek prodejní objednávky**. Sledování událostí objednávek slouží pro účely auditu, ke kontrole akcí provedených na objednávce během životního cyklu objednávky nebo ke sledování akcí konkrétního uživatele. Například můžete zaznamenat akci pokaždé, když uživatel vytvoří prodejní objednávku, objednávky blokuje, přepíše náklady nebo aktualizuje řádek objednávky. Události objednávky můžete nastavit pro sledování akcí pro konkrétního uživatele, skupinu uživatelů nebo všechny uživatele během určitého období. Akce, které byly zdokumentovány, můžete zobrazit otevřením stránky **Události objednávek** z podokna Akce na stránce daného dokumentu. Události objednávky můžete konfigurovat v nabídce **Prodej a marketing** &gt; **Nastavení** &gt; **Události** &gt; **Události objednávky**. Pokud nelze objednávku odběratele expedovat včas, společnost může automaticky odeslat e-mailové zprávy oznámení odběrateli pro vysvětlení stavu objednávky a poskytnutí odběrateli možnost zrušit objednávku. Pokud zpoždění přesahuje zadaný práh, může být objednávka zrušena automaticky. Až tři e-mailové zprávy lze odeslat v zadaných intervalech:

1.  **První upozornění na zrušení** – zákazník se může rozhodnout zrušit objednávku.
2.  **Druhé upozornění na zrušení** – zákazník se může rozhodnout zrušit objednávku.
3.  **Poslední upozornění na zrušení** – systém zruší objednávku a odběratel je informován o zrušení.

Můžete vyloučit jednotlivé odběratele a produkty z procesu automatického oznámování a stornování. Výstraha marže se spustí při přidání položky do objednávky. Výstraha obsahuje důležité informace o položce, jako je výše marže a ziskovosti položky. Tyto informace slouží k rozhodnutí, zda je přepsání ceny vhodné při přidání položky do prodejní objednávky. Můžete například nastavit prahové hodnoty pro obchodní marže a zadat tak, že náklady 40 % nebo více jsou pro položku přijatelné, ale prahová hodnota nákladů 20 až 39 procent je sporná. V tomto případě všechny položky, které mají prahovou hodnotu mezi hodnotami 20 a 39 procenty spustí výstrahu. Nelze prodat jakoukoliv položku, která má prahovou hodnotu nižší než 20 procent nad náklady a cenu položky nelze upravit. Můžete konfigurovat výstrahy marže v nabídce **Pohledávky** &gt; **Nastavení** &gt; **Parametry pohledávek** &gt; **Výstrahy marže**. Při nastavení přiřazení DPH na základě výchozích pravidel můžete určit prioritu párování pro prvky adresy. Lze například určit, aby párování skupiny DPH podle PSČ nebo kódu ZIP mělo vyšší prioritu než párování skupiny DPH podle státu. Při zadávání nových záznamů adres odběratele je skupina DPH přiřazena automaticky na základě toho, jak odpovídá adresa zákazníka výchozím pravidlům a prioritě párování, které jste definovali. Tuto funkci lze konfigurovat na stránce **Parametry hlavní knihy**.




