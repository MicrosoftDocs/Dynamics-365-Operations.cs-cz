---
title: Zabezpečení uživatele portálu pro dodavatele
description: V tomto článku se vysvětluje, jak nastavit zabezpečení pro externí dodavatele, kteří používají portál pro dodavatele. Informace v tomto tématu platí pouze pro verze aplikace Dynamics AX z února a května 2016.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2b95d386dd12bb1cb3577c3820b0be82d28df8e
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188481"
---
# <a name="vendor-portal-user-security"></a>Zabezpečení uživatele dodavatelského portálu

[!include [banner](../includes/banner.md)]

V tomto článku se vysvětluje, jak nastavit zabezpečení pro externí dodavatele, kteří používají portál pro dodavatele. Informace v tomto tématu platí pouze pro verze aplikace Dynamics AX z února a května 2016.

Funkce portálu dodavatele byla v Dynamics 365 for Operations verze 1611 nahrazena rozšířenou funkcí spolupráce dodavatelů. Další informace o nastavení zabezpečení pro dodavatelskou spolupráci naleznete v tématu [Nastavení a správa dodavatelské spolupráce](set-up-maintain-vendor-collaboration.md). Portál pro dodavatele poskytuje omezenou sadu informací o nákupních objednávkách (POs) pro externí dodavatele. Je důležité, aby byla správně nastavena oprávnění uživatelů k portálu pro dodavatele v aplikaci Microsoft Dynamics AX, aby dodavatelé neměli nežádoucí přístup k dalším informacím v instalaci aplikace Dynamics AX. **Upozornění:** Na rozdíl od jiných uživatelů externí dodavatelé nemají roli **Systémový uživatel**. Role **Systémový uživatel** poskytuje přístup ke skupině oprávnění, která nejsou vhodná pro externí uživatele.

## <a name="setting-up-a-vendor-portal-user"></a>Nastavení uživatele dodavatelského portálu
Před vytvořením uživatelského účtu pro někoho, kdo bude používat portál pro dodavatele, musíte povolit dodavatele pro spolupráci s portálem pro dodavatele. Použijte pole **Spolupráce v rámci nákupní objednávky** na kartě **Obecné** na stránce **Dodavatelé**. Externí dodavatelé, kteří používají portál pro dodavatele musí mít následující nastavení:

-   Účet uživatele MicrosoftAzure Active Directory (AAD) musí být registrován pro dodavatele na stránce **Uživatelé** v aplikaci Dynamics AX.
-   Dodavatel musí mít role zabezpečení **Dodavatel (externí)**, ne roli **Systémový uživatel**. **Poznámka:** Role **Systémový uživatel** je automaticky přidělena, když vytvoříte nový účet uživatele v aplikaci Dynamics AX. Proto je nutné odebrat tuto roli a potvrdit varovnou zprávu, která se zobrazí.
-   Dodavatelský uživatel nemá oprávnění k přidání dalších polí z tabulky nákupní objednávky do jejich zobrazení nákupní objednávky. Na kartě **Přizpůsobení** na kartě **Uživatelé**, nastavte možnost **Explicitní individuální nastavení je povoleno** pro uživatele na **Ne**.
-   Uživatelský účet musí být přidružen k registrované kontaktní osobě. Na stránce **Uživatelé** vyberte kontaktní osobu v poli **Jméno**. Osoba, kterou vyberete, má mít roli **Kontakt** pro příslušného dodavatele.

Jestliže stejná osoba vyžaduje přístup k portálu pro dodavatele pro více dodavatelských účtů (případně pro jiné právnické osoby), jednotlivé účty dané osoby uživatele být přidruženy ke stejné registrované kontaktní osobě. Role **Dodavatel (externí)** obsahuje všechny základní funkce, které jsou zapotřebí k používání funkce, které jsou k dispozici na portálu pro dodavatele. Toto nastavení pomáhá zajistit, že uživatelské rozhraní, které externí uživatel vidí, se zaměřuje pouze na očekávané scénáře.

## <a name="additional-resources"></a>Další zdroje

[Spolupráce s dodavateli pomocí portálu pro dodavatele](collaborate-vendors-vendor-portal.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]