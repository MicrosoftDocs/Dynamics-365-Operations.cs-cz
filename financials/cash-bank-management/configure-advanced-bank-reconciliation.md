---
title: "Přehled rozšířeného odsouhlasení banky"
description: "Rozšířené odsouhlasení banky můžete importovat elektronické bankovní výpisy a automaticky odsouhlasit s bankovními transakcemi v 365 Microsoft Dynamics pro operace.  Tento článek vysvětluje nastavení procesů odsouhlasení."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: c2fc9e858f61d7d0122393bbf306ba64ac3659b8
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Přehled rozšířeného odsouhlasení banky

[!include[banner](../includes/banner.md)]


Rozšířené odsouhlasení banky můžete importovat elektronické bankovní výpisy a automaticky odsouhlasit s bankovními transakcemi v 365 Microsoft Dynamics pro operace.  Tento článek vysvětluje nastavení procesů odsouhlasení.  

Existuje několik kousků, které musí být nastaveny před použitím funkce Rozšířené bankovního odsouhlasení. Další informace o nastavení import bankovního výpisu naleznete v tématu [nastavit proces importu výpisu banky](set-up-advanced-bank-reconciliation-import-process.md).  Požadavky na nastavení procesu odsouhlasení jsou podrobně popsány níže.

## <a name="transaction-codes"></a>Kódy transakce
Kódy transakcí lze použít jako součást pravidla párování pro odsouhlasení banky.  Kódy transakcí vám pomůže tak, aby odpovídala stejné typy transakcí mezi Dynamics 365 pro operace a bankovní výpis.  Provedení tohoto typu odpovídající je nutné nejprve definovat typy transakcí pro bankovní transakce z 365 Dynamics pro operace a potom namapovat tyto typy kódů transakcí výkazu bankou.  Typy transakcí pro Dynamics 365 pro bankovní operace transakce jsou definovány **typ bankovní transakce** stránky.  To je také kde můžete definovat hlavní účet pro účtování přiřazený k tomuto typu transakce. 

Jakmile jsou definovány aplikace Dynamics 365 pro kódy transakce bankovních operací, potom namapujte na kódy transakcí používané ve vaší elektronické bankovní výpisy.  Tento proces mapování se provádí pomocí **mapování kódu transakce** stránky.  Mapování kódu transakce je dokončena samostatně pro každý bankovní účet.

## <a name="matching-rules-and-matching-rule-sets"></a>Pravidla spárování a sady pravidel párování
Pravidla pro porovnávání umožňují definovat kritéria pro automatické odsouhlasení mezi Dynamics 365 pro operace bankovních transakcí a transakcí bankovního výpisu.  Nastavit pravidla pro porovnávání se provádí na **pravidla párování pro odsouhlasení** stránky.  Další informace naleznete v tématu [nastavit pravidla párování pro odsouhlasení banky](set-up-bank-reconciliation-matching-rules.md). 

Sady pravidel párování se používají k definování skupiny pravidla porovnávání, která se spustí v pořadí během odsouhlasení banky.  Sady pravidel párování jsou konfigurovány na **sady pravidel párování pro odsouhlasení** stránky.

## <a name="cash-and-bank-management-parameters"></a>Parametry pokladny a banky
Počet parametrů jsou specifické pro proces rozšířené bankovního odsouhlasení na **parametry řízení hotovosti a banky** stránky.  **Částka řádku výpisu zobrazit na straně má dáti/Dal** změní na zobrazení částek **bankovní výpis** stránky.  Pokud je vybrána tato možnost, zobrazí se v samostatné MD a Dal sloupcích částky transakce bankovního výpisu.  Pokud není zaškrtnuto, budou částky transakce bankovního výpisu jednotná částka sloupce s příslušnou značkou. 

Možnosti ověřování, které jsou nastaveny na stránce parametry přepsat vybrané položky nastavit na odpovídající pravidla.  Například nelze ručně nebo automaticky spáruje dokumenty nad rámec na stránce parametry nastavit datum rozdíl.  Také pokud možnost **ověřit mapování pro typ transakce** je vybrána, typy transakcí musí být mapována mezi 365 Dynamics pro bankovní operace transakce a transakce bankovního výpisu v pořadí pro transakce ručně nebo automaticky odpovídat. 

Je také nutné nakonfigurovat potřebné číselné řady v **parametry řízení hotovosti a banky** stránky.  Na **číselné řady** kartě kódy nastavit číselné řady pro stahování **ID, ID výkazu, Odsouhlasit ID a bankovního odsouhlasení** odkazy.

## <a name="bank-account-reconciliation-options"></a>Možnosti odsouhlasení bankovního účtu
Je nutné nejprve povolit rozšířené odsouhlasení banky pro bankovní účet.  Některé další možnosti jsou k dispozici na **bankovního účtu** stránky, jakmile je povolena funkce Rozšířené bankovního odsouhlasení. 

**Použití bankovní výpisy jako potvrzení elektronické platby** funkce je integrována funkce odsouhlasení banky stavy elektronické platby.  Pokud je tato možnost povolena, bankovní dokument se automaticky vytvoří pro elektronické platby stav nastaven na **odeslané**.  Kromě toho stav elektronické platby bude aktualizován z **odeslané** k **přijato** po zaplacení je obsažena, odsouhlasen a zaúčtovány. 

**Název bankovního účtu v příkazech** pole je název používaný pro bankovní účet ve vaší elektronické bankovní výpisy.  Tento název se používá při určování transakcí, které chcete importovat bankovního účtu z příkazu, který může obsahovat informace pro více bankovních účtů. 

Možnost **po importu odsouhlasit** bude automaticky ověřit bankovní výpis, vytvořte nové odsouhlasení bankovního účtu a listu a spustit výchozí odpovídající sadu pravidel.  Tato funkce automatizuje proces až k bodu transakcí, které jsou ručně přiřazeny.  Při importu bude nastaven jako výchozí nastavení v položce bankovního účtu.




