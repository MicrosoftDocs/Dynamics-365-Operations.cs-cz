---
title: Vytvoření volných faktur
description: Toto téma vysvětluje, jak vytvořit volné faktury.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 4498f5c9ce0e3830ffe1857c0363ca962561fc59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176841"
---
# <a name="create-free-text-invoices"></a>Vytvoření volných faktur

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit volné faktury. Pro proceduru použijte ukázkovou společnost **USMF**.

## <a name="create-a-free-text-invoice"></a>Vytvořit volnou fakturu

1. Přejděte na **Pohledávky \> Faktury \> Všechny volné faktury**.
2. Vyberte možnost **Nový**.
3. V poli **Účet odběratele** vyberte hodnotu.

    * Ve výchozím nastavení se jako účet faktury použije účet, který je zvolen jako účet odběratele.
    * Pokud nebyla faktura zaúčtována, počátečním účetním stavem je **Zpracovává se**.
    * Číslo faktury bude přiřazeno při zaúčtování faktury.
    * Pokud používáte zmocnění SEPA, bude při výběru účtu zákazníka automaticky vyplněno zmocnění.

4. V poli **Popis** zadejte hodnotu.
5. V poli **Hlavní účet** zadejte číslo účtu, které nemá dimenze. Dimenze zadáte později v tomto tématu.

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
    * Volbou možnosti **Ano** vytisknete fakturu.
    * Volbou možnosti **Ano** zaúčtujete fakturu. Fakturu můžete vytisknout bez jejího zaúčtování.

19. Vyberte **OK**.

## <a name="copy-lines"></a>Kopírovat řádky
Chcete-li zkopírovat řádky volné faktury, vyberte jeden nebo více řádků a zvolte **Kopírovat vybrané řádky**. Můžete určit počet kopií, které chcete vytvořit, a můžete také zkopírovat poznámky a přílohy. Můžete buď zkopírovat distribuce nebo umožnit jejich opětovné vytvoření při zaúčtování.

Jakmile zkopírujete řádky, lze podle potřeby upravit informace.

## <a name="create-a-free-text-invoice-from-a-template"></a>Vytvoření volné faktury ze šablony
Můžete vytvořit volnou fakturu ze šablony. Vyberete-li **Nová ze šablony** na kartě **Faktura**, můžete vybrat název šablony a účet odběratele pro novou volnou fakturu. Výchozí hodnoty, jako jsou například platební podmínky a způsob platby, lze automaticky vyplnit z odběratele, nebo můžete použít hodnoty, které byly uloženy v šabloně.

Bude vytvořena nová volná faktura a můžete upravit hodnoty podle potřeby.
