---
title: Povolit správu změn u stávajících produktů
description: Toto téma vysvětluje, jak můžete povolit správu změn u stávajících produktů. Popisuje také případy, kdy je vaše schopnost povolit správu změn omezená.
author: t-benebo
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f0fba0a9234e5b7cb055f7b97578bff72f1d06ac
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571970"
---
# <a name="enable-change-management-on-existing-products"></a>Povolit správu změn u stávajících produktů

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak můžete povolit správu změn u stávajících produktů. Popisuje také případy, kdy je vaše schopnost povolit správu změn omezená.

Když povolíte správu změn pro existující produkt, můžete vytvářet verze tohoto produktu a sledovat změny, které jsou v něm provedeny po celou dobu jeho životnosti. Proto můžete tyto změny sledovat pomocí změnových příkazů. Chcete-li povolit správu změn, musíte převést příslušné produkty na *technické položky* (označované také jako technické produkty). Technické produkty jsou produkty, u kterých existují různé verze, které jsou řízeny prostřednictvím správy změn. K dispozici je průvodce, který vás provede procesem převodu.

## <a name="turn-on-the-feature-in-your-system"></a>Zapnutí funkce ve vašem systému

Chcete-li používat tuto funkci, je nutné dokončit následující kroky:

1. Povolte funkci správy technických změn a její konfigurační klíč, jak je popsáno v [Přehledu správy technických změn](product-engineering-overview.md).
1. Zapněte možnost *Povolit správu změn u stávajících produktů* ve správě funkcí. Další informace naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="restrictions-and-limitations"></a>Omezení a limity

Ne všechny typy produktů lze převést na všechny ostatní typy. Platí následující omezení a limity:

- Když převedete produkt na technický produkt, zůstane *produktem*. Nestává se *základním produktem*.
- Když převádíte základní produkt, který má určitou sadu dimenzí, tyto dimenze se po změně zachovají. Například pokud převedete základní produkt, který má dimenzi velikosti, zachová si dimenzi velikosti.

Pokud tedy máte odlišný produkt, můžete jej změnit pouze na technický produkt, který nesleduje dimenzi produktu v transakcích (tj. dimenze verze se nepoužívá). Další informace o těchto záležitostech naleznete v následujících částech tohoto tématu.

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a>Připravte se na převod vytvořením všech požadovaných kategorií technických produktů

*Kategorie technických výrobků* musí být přiřazena ke každému technickému produktu. Toto přiřazení provedete při spuštění průvodce **Převést na technický produkt**. Pro všechny příslušné standardní produkty musejí existovat kategorie technických produktů *předtím*, než tyto produkty převedete.

Kategorie technického produktu poskytuje základ pro vytvoření technického produktu a zavádí sadu výchozích hodnot a zásad. Technické atributy a jejich výchozí hodnoty (jak jsou definovány pro technickou kategorii) jsou také použity na výsledný technický produkt. Hodnoty atributů můžete podle potřeby upravit nebo přidat do výsledného produktu další technické atributy.

Kategorie technického produktu musí odpovídat produktu, ke kterému ji přiřadíte. Například typ produktu a skupina dimenzí musí odpovídat produktu i jeho kategorii technického produktu. Více informací naleznete v části [Technické verze a kategorie technických produktů](engineering-versions-product-category.md).

> [!IMPORTANT]
> Průvodce **Převést na technický produkt** může převést produkt pouze na technické produkty, u kterých není verze sledována v transakcích. Proto musí být možnost **Sledovat verzi v transakcích** nastavena na *Ne* u kategorií technických produktů, které vytvoříte pro převod existujících produktů.

Další informace o vytváření kategorií technických produktů najdete v části [Technické verze a kategorie technických produktů](engineering-versions-product-category.md).

## <a name="run-the-convert-to-engineering-product-wizard"></a>Spuštění průvodce Převést na technický produkt

Průvodce **Převést na technický produkt** vám pomůže převést jeden nebo více stávajících produktů na technické produkty. Převádí produkty na technické produkty (verzované produkty), kde verze není sledována v transakcích (tj. dimenze verze se nepoužívá). Po dokončení převodu můžete produkty spravovat pomocí funkce Správa technických změn.

Převod je trvalý. Proto ho není možné později stornovat. 

Každý převedený technický produkt bude i nadále vydáván ve stejných společnostech, ve kterých byl vydán původní produkt. Technické kusovníky a trasy však nebude těmto společnostem automaticky vydány.

Podle následujících pokynů spusťte průvodce **Převést na technický produkt** a převeďte produkt na technický produkt.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. V mřížce zaškrtněte políčko u každého produktu, který chcete převést.
1. V podokně akcí na kartě **Analýza** ve skupině **Správa technických změn** otevřete průvodce výběrem možnosti **Převést na technický produkt**.
1. První stránka průvodce se jmenuje **Vítejte**. Pokud ještě nejste obeznámeni s procesem převodu, pečlivě si přečtěte informace na této stránce. Jakmile budete připraveni k pokračování, vyberte **Další**.
1. Stránka **Vyberte podrobnosti produktů, které mají být převedeny** zobrazuje každý produkt, který jste vybrali před spuštěním průvodce. Prohlédněte si seznam. Pomocí tlačítek **Nový** a **Odstranit** na panelu nástrojů přidejte nebo odeberte podle potřeby produkty.
1. Pomocí následujících polí v horní části mřížky můžete přiřadit výchozí hodnoty každému produktu, který je na seznamu. (Tyto hodnoty budete moci u jednotlivých produktů změnit po dokončení převodu.) Výchozí hodnoty nebudou přiřazeny produktům, kterým již byla přiřazena příslušná hodnota.

    - **Výchozí technická kategorie** – Vyberte počáteční kategorii technického produktu, kterou chcete přiřadit ke každému uvedenému produktu. Kategorie, kterou vyberete, bude použita pouze u produktů, které jsou s ní kompatibilní.
    - **Výchozí verze** – Zadejte počáteční verzi produktu, kterou chcete přiřadit ke každému uvedenému produktu. Každý technický produkt má alespoň jednu technickou verzi.
    - **Výchozí stav životního cyklu** – Vyberte počáteční stav životního cyklu produktu, který chcete přiřadit ke každému uvedenému produktu.
    - **Aktuální kusovník bude součástí technického produktu** – Zaškrtněte toto políčko, pokud má být aktuální kusovník pro každý uvedený produkt použit jako kusovník pro technický produkt.

    Další informace o nastavení produktu naleznete v dalším kroku.

1. Zkontrolujte každý produkt, který je uveden v mřížce, a vyhodnoťte, jak dobře se na něj vztahují výchozí hodnoty, které jste přiřadili. U každého řádku zkontrolujte následující informace a nastavte příslušná pole:

    - **Číslo produktu** – Číslo produktu.
    - **Název produktu** – Název produktu.
    - **Technická kategorie** – Vyberte kategorii technického produktu, do které by měl produkt po převodu patřit. Jak již bylo vysvětleno v předchozí části tohoto tématu, pro každý produkt již musí existovat příslušná kategorie. Každému produktu musíte přiřadit kategorii.
    - **Verze** – Zadejte verzi produktu, kterou chcete přiřadit k produktu po jeho převodu. Můžete například vybrat číslo, které odpovídá číselné řadě, kterou vaše kategorie již používá. Každá technická verze ukládá technická data, která jsou specifická pro tuto verzi. Více informací naleznete v části [Technické verze a kategorie technických produktů](engineering-versions-product-category.md).
    - **Stav životního cyklu produktu** – Vyberte stav životního cyklu produktu, ve kterém by měl být produkt po převodu. Stav životního cyklu produktu vám umožňuje určit, které transakce jsou pro danou technickou verzi povoleny. Další informace viz [Stavy životního cyklu produktu a transakce](product-lifecycle-state-transactions.md).
    - **Má kusovník** – Vybrané zaškrtávací políčko označuje, že produkt má kusovník. Nastavení tohoto zaškrtávacího políčka vám může pomoci rozhodnout se, jak nastavit zaškrtávací políčko **Aktuální kusovník bude součástí technického produktu**.
    - **Aktuální kusovník bude součástí technického produktu** – Zaškrtněte toto políčko, pokud má být aktuální kusovník produktu použit jako kusovník pro technický produkt. Tento kusovník pak bude řízen funkcí Správa technických změn. Pokud produkt nemá kusovník nebo pokud dáváte přednost pozdějšímu ručnímu vytvoření kusovníku pro převedený produkt, zrušte zaškrtnutí tohoto políčka.
    - **Má chyby** – Vybrané zaškrtávací políčko označuje, že nastavení produktu obsahuje jednu nebo více chyb. Například typ produktu nebo skupina dimenzí se nemusí v kategorii shodovat. Produkty, které obsahují chyby, budou přeskočeny a nebudou převedeny.

1. Po dokončení vyberte na panelu nástrojů možnost **Ověřit**, aby došlo k ověření nastavení produktu. U každého řádku bude zaškrtávací políčko **Má chyby** aktualizováno, aby ukazovalo stav produktu. Upravujte hodnoty, dokud nebude nastavení každého produktu bez chyb.
1. Když jsou všechny produkty správně nastaveny, pokračujte výběrem možnosti **Další**.
1. Stránka **Potvrďte výběr** zobrazuje počet produktů, které nemají žádné chyby v nastavení, a jsou proto připraveny k převodu. Zobrazuje také počet produktů, které budou kvůli chybám vynechány. Chcete-li spustit převod jako dávkovou úlohu, nastavte možnost **Spustit v dávce** na *Ano*.
1. Výběrem možnosti **Dokončit** použijete nastavení a spustíte převod produktů na technické produkty.

> [!NOTE]
> Pokud má váš systém nastaveno ruční schvalování produktů před jejich vydáním, musíte každý převedený produkt schválit na stránce **Otevřené verze produktů** v příslušných společnostech. Více informací najdete v tématu [Než produkt vydáte v místní společnosti, zkontrolujte jej a přijměte](engineering-scenarios.md#accept).
