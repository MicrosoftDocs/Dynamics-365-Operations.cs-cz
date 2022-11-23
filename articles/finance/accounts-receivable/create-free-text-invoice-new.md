---
title: Vytvořit volnou fakturu
description: Tento článek vysvětluje, jak vytvořit volné faktury.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 4298d7114e0237072c242e83e51951a922e34e5a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780465"
---
# <a name="create-a-free-text-invoice"></a>Vytvořit volnou fakturu

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak vytvořit volné faktury. Pro proceduru použijte ukázkovou společnost **USMF**.

## <a name="create-a-free-text-invoice"></a>Vytvořit volnou fakturu

1. Přejděte na **Pohledávky \> Faktury \> Všechny volné faktury**.
2. Vyberte možnost **Nový**.
3. V poli **Účet odběratele** vyberte hodnotu.

    * Ve výchozím nastavení se jako účet faktury použije účet, který je zvolen jako účet odběratele.
    * Pokud nebyla faktura zaúčtována, počátečním účetním stavem je **Zpracovává se**.
    * Číslo faktury bude přiřazeno při zaúčtování faktury.
    * Pokud používáte zmocnění SEPA, bude při výběru účtu zákazníka automaticky vyplněno zmocnění.

4. V poli **Popis** zadejte hodnotu.
5. V poli **Hlavní účet** zadejte číslo účtu, které nemá dimenze. Dimenze zadáte později v tomto článku.

    Můžete také zadat jeden nebo více znaků pro hlavní účet a vyhledat účet pomocí vyhledávání.

6. Zvolte pevnou záložku **Podrobnosti řádku**, aby bylo možné přidat dimenze do hlavního účtu.
7. Zvolte karu **Řádek finančních dimenzí**.

    * Dimenze jsou pouze pro vybraný řádek.
    * Výchozí skupina DPH je vyplněna z odběratele. Pokud odběratel nemá skupinu DPH, použije se skupina DPH z hlavního účtu.
    * Skupina DPH položek je vyplněna z hlavního účtu. Pokud hlavní účet nemá skupinu DPH položky, použije se skupina DPH položky určená v parametrech v hlavní knize.

8. Volitelné: Zadejte číslo do pole **Množství**.
9. Volitelné: Zadejte číslo do pole **Jednotková cena**.

    Částka se počítá jako součin množství a jednotkové ceny. Výpočet však lze přepsat zadáním částky.

10. Zvolte **DPH** pro zobrazení DPH, která bylo pro fakturu vypočtena.

    Na této stránce můžete zobrazit částky DPH nebo je můžete přepsat na kartě **Úprava**.

11. Vyberte **OK**.
12. Zvolte **Náklady**, pokud chcete přidat náklady do faktury.
13. Zadejte hodnotu do pole **Kód nákladů**.
14. Zadejte číslo do pole **Hodnota nákladů**.
15. Zavřete stránku.
16. Zvolte **Součty** pro zobrazení podrobností a celkové částky souhrnné faktury.
17. Vyberte **Zavřít**.
18. Vyberte **Zaúčtovat** pro zaúčtování faktury. Stále budete mít možnost zrušení před skutečným účtováním.

    * Můžete změnit časování tisku faktury. Výběrem **Aktuální** vytisknete jednotlivé faktury při aktualizaci. Výběrem **Po** vytisknete všechny faktury po aktualizaci.
    * Pokud chcete změnit ověření limitu úvěru odběratele před zaúčtováním faktury, změňte hodnoty v **typ limitu úvěru** pole.
    * Na kartě **Aktualizace** ve stránce **Parametry pohledávek** (**Pohledávky > Nastavení > Parametry pohledávek**) můžete zastavit účtování volných faktur, když nastane chyba. Výběrem možnosti **Ano** u parametru **Zastavit účtování volných faktur při první chybě** zastavíte účtování volných faktur, když dojde k chybě. Pokud účtujete v dávce, chyba zastaví proces účtování a stav dávky bude nastaven na **Chyba**. Pokud tato možnost není vybrána, proces zaúčtování přeskočí fakturu s chybou zaúčtování a bude pokračovat v zaúčtování dalších faktur. Pokud účtujete v dávce, chyba účtování nezabrání v zaúčtování dalších faktur. Stav dávky bude **Skončeno**. Podrobná zpráva o procesu zaúčtování bude k dispozici ke kontrole v historii dávkové úlohy.
    * Volbou možnosti **Ano** vytisknete fakturu.
    * Volbou možnosti **Ano** zaúčtujete fakturu. Fakturu můžete vytisknout bez jejího zaúčtování.

19. Vyberte **OK**.

## <a name="copy-lines"></a>Kopírovat řádky
Chcete-li zkopírovat řádky volné faktury, vyberte jeden nebo více řádků a zvolte **Kopírovat vybrané řádky**. Můžete určit počet kopií, které chcete vytvořit, a můžete také zkopírovat poznámky a přílohy. Můžete buď zkopírovat distribuce nebo umožnit jejich opětovné vytvoření při zaúčtování.

Jakmile zkopírujete řádky, lze podle potřeby upravit informace.

## <a name="create-a-free-text-invoice-from-a-template"></a>Vytvoření volné faktury ze šablony
Můžete vytvořit volnou fakturu ze šablony. Vyberete-li **Nová ze šablony** na kartě **Faktura**, můžete vybrat název šablony a účet odběratele pro novou volnou fakturu. Výchozí hodnoty, jako jsou například platební podmínky a způsob platby, lze automaticky vyplnit z odběratele, nebo můžete použít hodnoty, které byly uloženy v šabloně.

Bude vytvořena nová volná faktura a můžete upravit hodnoty podle potřeby.

## <a name="resetting-the-workflow-status-for-free-text-invoices-from-unrecoverable-to-draft"></a>Resetování stavu pracovního postupu pro volné faktury z Bez možnosti obnovy na Koncept
Instance workflow, která byla zastavena kvůli neobnovitelné chybě, bude míst stav workflow **Bez možnosti obnovy**. Pokud je pracovní postup volné faktury odběratele ve stavu **Bez možnosti obnovy**, můžete ho obnovit do stavu **Koncept** výběrem možnosti **Obnovit** v akcích pracovního postupu. Poté můžete volnou fakturu odběratele upravit. Tato funkce je k dispozici, pokud je zapnutý parametr **Resetování stavu pracovního postupu pro volné faktury z Bez možnosti obnovy na Koncept** na stránce **Správa funkcí**.

Na stránce **Historie workflowu** můžete resetovat stav workflow na **Koncept**. Tuto stránku můžete otevřít z **Volné faktury** nebo z nabídky **Obecné > Dotazy > Pracovní postup**. Chcete-li obnovit stav workflow na **Koncept**, vyberte možnost **Obnovit**. Stav pracovního postupu můžete také resetovat na **Koncept** výběrem akce **Obnovit** na stránce **Volná faktura** nebo **Všechny volné faktury**. Po resetování stavu pracovního postupu na **Koncept** bude k dispozici pro úpravy na stránce **Volná faktura**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
