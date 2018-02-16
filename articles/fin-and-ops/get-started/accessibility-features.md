---
title: "Funkce usnadnění přístupu"
description: "Toto téma popisuje funkci, která je určená k tomu, aby pomohla uživatelům, kteří mají různá postižení, používat aplikace Dynamics 365 for Finance and Operations, Enterprise edition, Dynamics 365 for Retail a Dynamics 365 for Talent."
author: TLeforMicrosoft
manager: AnnBe
ms.date: 01/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a523ff097eedf9a4a2cb0341b3be9d05abfa09fa
ms.openlocfilehash: 42b4f670dee95c073ce8dcca16afef83bbf78ff8
ms.contentlocale: cs-cz
ms.lasthandoff: 01/23/2018

---

# <a name="accessibility-features"></a>Funkce usnadnění přístupu

Toto téma popisuje funkci, která je určená k tomu, aby pomohla uživatelům, kteří mají různá postižení, používat aplikace Dynamics 365 for Finance and Operations, Enterprise edition, Dynamics 365 for Retail a Dynamics 365 for Talent. Existují například funkce pro zrakově postižené uživatele, kteří používají technologie jako je Microsoft Windows Narrator

## <a name="windows-narrator-and-keyboard-only-access"></a>Windows Narrator a přístup pouze pomocí klávesnice

Každé pole a ovládací prvek má popisek a popis použitelných zkratek. Čtečka obrazovky může přečíst štítek a popis.

## <a name="shortcuts-for-the-most-frequently-performed-actions"></a>Zkratky pro nejčastěji prováděné akce

Pro většinu uživatelů zahrnuje každodenní používání systému velké množství zadávání dat a interakce s klávesnicí. Pro vylepšení uživatelského prostředí jsme vytvořili zkratky umožňující "skákat" kolem obrazovky a zkratky pro speciální akce. Další informace naleznete v tématu [Klávesové zkratky](shortcut-keys.md). 

## <a name="navigation-search"></a>Hledání za účelem navigace

Každá stránka, ke které se přistupuje pomocí nabídky navigačního podokna, podokna nejvíce vlevo, je rovněž dostupná z pole **Vyhledávání**. Stisknutím kláves Alt + G přesunete výběr na pole **Vyhledávání** a pak můžete zadat název nebo popis stránky.

!["Bankovní účet" zadaný do pole vyhledávání](media/6d08b0be32808221023e2aa92d69fd70.png)

Další informace naleznete v tématu [Hledání za účelem navigace](navigation-search.md).

> [!NOTE]
> Můžete přecházet přímo pouze na stránky nejvyšší úrovně. Sekundární stránky využívají informace nebo kontext z jejich nadřazené stránky.

## <a name="action-search-for-keyboard-only-users-or-for-heads-down-data-entry"></a>Vyhledávání akce pro uživatele s klávesnicí nebo pro zadávání dat bez ověření chybovosti

Ke každé akci, kterou nabízí stránka, se lze dostat z klávesnice pomocí posloupnosti karet. Informace o posloupnosti karet jsou poskytnuty dále v tomto tématu. Abyste mohli spustit akce přímějším způsobem, můžete použít funkci vyhledávání akce.

### <a name="example"></a>Příklad

Chcete spustit akci **Protokol oznámení e-mailem**, která se zobrazí ve skupině **Oznámení e-mailem** na kartě **Prodejní objednávka** v podokně akcí.

![Akce protokolu oznámení e-mailem v podokně akcí](media/f0d78399e7fafcd85ded1cd1e3d34f3c.jpg)

Jedna z možností je použití klávesnice. Stisknutím kombinace kláves Ctrl + F6 přesuňte výběr na podokno akcí a poté stiskněte opakovaně klávesu Tab, abyste se přesunuli přes všechny karty a akce až na výběr akce **Protokol oznámení e-mailem**.

Můžete také spustit akci přímějším způsobem. Kdekoliv na stránce stiskněte kombinaci kláves Ctrl + apostrof a zobrazí se pole vyhledávání akcí.

![Vyhledávací pole akcí](media/80f7e8c5ac412fdf2c8a12f7728f135a.jpg)

V poli pro vyhledávání zadejte slova, která popisují akci. Tato akce vám bude k dispozici a lze ji spustit přímo. Například zadáním slov **e-mail**, **oznám** (částečné slovo), nebo **protokol**, je možné "přeskočit" na funkci protokolu oznámení e-mailem.

!["E-mail" zadaný do pole vyhledávání](media/image4.png) !["Oznám" zadané do pole vyhledávání](media/image5.png) !["Protokol" zadaný do pole vyhledávání](media/image6.png)

Po dokončení můžete stisknout kombinaci kláves Ctrl + apostrof znovu a vrátit výběr na pole, se kterým jste pracovali před spuštěním hledání akce.

Další informace naleznete v tématu [Vyhledání akce](action-search.md).

## <a name="tab-sequence"></a>Posloupnost karet

Při každodenním použití systému nejsou třeba k provádění typických úloh všechna pole. Proto je standardně posloupnost karet optimalizována. Zarážky karet jsou nastaveny pouze na těch polích, která jsou důležitá pro typické scénáře.

Můžete však zjistit, že některá pole, která často používáte k provádění úloh, nejsou zahrnuta ve výchozí posloupnosti karet. V takovém případě, používáte-li Windows Narrator, můžete použít jeho akce klávesnice pro přístup k těmto polím a kontrole jejich obsahu. Případně je můžete zapnout možnost **Rozšířená posloupnost karet** na stránce **Možnosti**. Tato možnost učiní všechny upravitelná pole a pole jen pro čtení součástí posloupnosti karet. Poté můžete použít individuální nastavení stránky k vytvoření vlastní posloupnosti karet a vyloučit pole, která nemusí být součástí posloupnosti karet. Další informace o individuálním nastavení najdete v části [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

![Možnost rozšířené posloupnosti karet](media/8c0f12bbb3f26032997ef0ba95d89b6a.png)

## <a name="form-patterns"></a>Vzory formulářů

Téměř 90 procent stránek v produktu je založeno na malé sadě vzorců. Tyto vzory se označují jako *vzorce formuláře*. Každý vzorec formuláře slouží k poskytnutí akcí, které jsou na stránce prováděny nejčastěji.  Vzorce formuláře pomáhá zajistit znalost a jednoduché pochopení, protože často používané akce a data se vždy nacházejí na stejném místě různých stránek. Z důvodu malého počtu vzorců formulářů se mohou uživatelé snadno tento systém naučit, bez ohledu na počet stránek, a poté ho s jistotou používat.

Další informace o vzorcích formuláře naleznete v tématu [Styly a vzory formulářů](../../dev-itpro/user-interface/form-styles-patterns.md).

## <a name="responsive-layout"></a>Interaktivní rozvržení

Produkt je navržen pro práci na různých zařízení a provedeních, od nejmenších obrazovek po velké obrazovky s nejvyšším rozlišením. Náš modul interaktivního rozvržení umožňuje uživatelům úroveň přiblížení 200 procent (a v některých případech více než 200 %).

## <a name="guidance-to-help-developers-and-customers-incorporate-accessible-thinking-in-their-customizations"></a>Pokyny pro vývojáře a odběratele k tomu, jak začlenit usnadnění přístupu do svých přizpůsobení

Další informace o osvědčených postupech společnosti Microsoft pro usnadnění přístupu naleznete v tématu [Dostupnost ve formulářích, produktech a ovládacích prvcích](../../dev-itpro/user-interface/enable-accessibility.md).

