---
title: Konfigurace sdílených parametrů
description: Musíte nastavit sdílené parametry pro záznamy, které jsou sdíleny napříč společnostmi, jako jsou například záznamy pozice. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů napříč právnickými osobami.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7aff01bee8cadcf852ae32fd60447c68e2174a2a
ms.sourcegitcommit: 43962e6fedaf55aab2f28f53bc38a69d2ff58403
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/01/2021
ms.locfileid: "6332988"
---
# <a name="configure-shared-parameters"></a>Konfigurace sdílených parametrů

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Musíte nastavit sdílené parametry pro záznamy, které jsou sdíleny napříč společnostmi, jako jsou například záznamy pozice. Tento článek vysvětluje, jak nastavit parametry lidských zdrojů napříč právnickými osobami.

Některé typy záznamů jako jsou například Záznamy pozice, jsou sdíleny mezi společnostmi. Pro tyto záznamy musíte nastavit sdílené parametry. Můžete například použít stránku **Sdílené parametry lidských zdrojů** k nastavení parametrů lidských zdrojů mezi právnickými osobami. 

Na stránce **Sdílené parametry lidských zdrojů** jsou seskupeny parametry do skupin podle jejich funkce. 

### <a name="settings"></a>Nastavení
Na kartě **Identifikace** je nutné vybrat typy identifikace, které představují identifikační čísla, která jsou uvedena na stránce. Typy identifikace musíte nastavit před zadáním identifikačních informací o zaměstnancích. Informace o čísle sociálního pojištění, národním identifikačním čísle, rodném čísle cizince a identifikační kód osoby jsou uvedeny na stránce **Typ identifikace**. Definujte nový typ identifikace nebo zkontrolujte seznam stávajících typů kliknutím na možnost **Správa personálu** &gt; **Karta Odkazy** &gt; **Nastavení** &gt; **Typy identifikace**. Můžete zadat jednoduchý kód a popis. 

Na kartě **Číselné řady** můžete vybrat číselné řady, které se používají pro následující záznamy: osobní číslo, pozice, ID požadavku uživatele, dokument I-9, uchazeč, diskuse, ID výhody a akce personálu (je-li povolen tento typ záznamu). Pro správu číselné řady odkazů a kódů, použijte stránky seznamu **Číselné řady**. Použijte funkci vyhledávání stránky, chcete-li tuto stránku najít. 

Na kartě **Pozice** určete, zda jsou k dispozici nové pozice pro přiřazení ve výchozím nastavení:

- **Nikdy** – Nemůžete přiřazovat pracovníky k novým pozicím při vytváření pozic. Při vytváření pozic se čas a datum položky **K dispozici pro přiřazení** na kartě **Obecné** stránky **Pozice** automaticky nastavuje na datum a čas vytvoření.
- **Niky** – Nemůžete přiřazovat pracovníky k novým pozicím při vytváření pozic. Pokud vyberete tuto možnost, musíte otevřít stránku **Pozice** pro každou novou pozici, jakmile bude k dispozici. Pak na kartě **Všeobecné** zadejte datum **K dispozici pro přiřazení** umožňující přiřazení pracovníků.

Na kartě **Pokročilý přístup** můžete omezit přístup k některým informacím nebo odkazům:

- **Omezit přístup k informacím o pracovníkovi** – Tuto funkci zapněte, pokud by uživatelé měli mít možnost zobrazit informace o zaměstnancích pouze u těch právnických osob, ke kterým mají přístup, a u zaměstnanců, kteří mají zaměstnání v těchto právnických osobách.

    Po zapnutí této funkce musíte podle těchto kroků nastavit příslušná oprávnění pro každého uživatele, jehož zobrazení musí být omezeno:

    1. Na stránce **Uživatelé** vyberte uživatele.
    1. Vyberte roli pro uživatele. Možnost **Přiřadit organizace** bude k dispozici.
    1. Vyberte **Přiřadit organizace**.
    1. Na nové stránce vyberte **Udělit přístup konkrétním organizacím individuálně** a poté vyberte organizace, ke kterým by měl mít uživatel přístup.
    1. Opakujte kroky 2 až 4 pro všechny ostatní role, které má uživatel, včetně role uživatele systému.

    > [!NOTE]
    > Společnosti, ke kterým má uživatel přístup, se musí shodovat ve všech rolích uživatele.

- **Povolit zobrazení kompenzace mezi společnostmi** – Odměny zaměstnancům se přiznávají za každou právnickou osobu v zaměstnání. Někdy může být zaměstnanec zaměstnán ve více právnických osobách současně. Když je tato funkce zapnutá, kompenzace za každou právnickou osobu se objeví v samoobslužných službách pro zaměstnance a samoobslužných službách pro správce, aniž by bylo nutné měnit právnické osoby. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
