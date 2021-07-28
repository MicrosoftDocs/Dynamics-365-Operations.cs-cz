---
title: Přepínání mezi návrhy dodavatele
description: Tohle téma popisuje způsob přepínání integrace dat dodavatele mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 70904ee716aabd019210e92895a894810bde27fb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346513"
---
# <a name="switch-between-vendor-designs"></a>Přepínání mezi návrhy dodavatele

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a>Tok dat dodavatele 

Pokud se rozhodnete použít tabulku **Účet** k ukládání dodavatelů typu **Organizace** a tabulku **Kontakt** k ukládání dodavatelů typu **Osoba**, nakonfigurujte následující workflowy. V opačném případě není tato konfigurace nutná.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Použití rozšířeného návrhu dodavatele pro dodavatele typu Organizace

Balíček řešení **Dynamics365FinanceExtended** obsahuje následující šablony procesu workflowu. Pro každou šablonu vytvoříte workflow.

+ Vytvoření dodavatelů v tabulce Účty
+ Vytvoření dodavatelů v tabulce Dodavatelé
+ Aktualizace dodavatelů v tabulce Účty
+ Aktualizace dodavatelů v tabulce Dodavatelé

Pro vytvoření nových procesů workflowu pomocí šablon procesů workflowu postupujte následovně.

1. Vytvořte proces pracovního postupu pro tabulku **Dodavatel** a vyberte šablonu procesu pracovního postupu **Vytvoření dodavatelů v tabulce Účty**. Pak vyberte **OK**. Tento workflow zpracovává scénář vytvoření dodavatele pro tabulku **Účet**.

    ![Proces pracovního postupu Vytvoření dodavatelů v tabulce Účty.](media/create_process.png)

2. Vytvořte proces pracovního postupu pro tabulku **Dodavatel** a vyberte šablonu procesu pracovního postupu **Aktualizace dodavatelů v tabulce Účty**. Pak vyberte **OK**. Tento workflow zpracovává scénář aktualizace dodavatele pro tabulku **Účet**.
3. Vytvořte proces pracovního postupu pro tabulku **Účet** a vyberte šablonu procesu pracovního postupu **Vytvoření dodavatelů v tabulce Dodavatelé**.
4. Vytvořte proces pracovního postupu pro tabulku **Účet** a vyberte šablonu procesu pracovního postupu **Aktualizace dodavatelů v tabulce Dodavatelé**.
5. Pracovní postupy můžete konfigurovat buď jako workflowy v reálném čase nebo na pozadí v závislosti na vašich požadavcích. Chcete-li nakonfigurovat workflow jako workflow na pozadí, vyberte možnost **Převést na workflow na pozadí**.

    ![Tlačítko Převést na workflow na pozadí.](media/background_workflow.png)

6. Aktivujte pracovní postupy, které jste vytvořili pro tabulky **Účet** a **Dodavatel**, abyste mohli začít používat tabulku **Účet** k ukládání informací pro dodavatele typu **Organizace**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Použití rozšířeného návrhu dodavatele pro dodavatele typu Osoba

Balíček řešení **Dynamics365FinanceExtended** obsahuje následující šablony procesu workflowu. Pro každou šablonu vytvoříte workflow.

+ Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé
+ Vytvoření dodavatelů typu Osoba v tabulce Kontakty
+ Aktualizace dodavatelů typu Osoba v tabulce Kontakty
+ Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé

Pro vytvoření nových procesů workflowu pomocí šablon procesů workflowu postupujte následovně.

1. Vytvořte proces pracovního postupu pro tabulku **Dodavatel** a vyberte šablonu procesu pracovního postupu **Vytvoření dodavatelů typu Osoba v tabulce Kontakty**. Pak vyberte **OK**. Tento workflow zpracovává scénář vytvoření dodavatele pro tabulku **Kontakt**.
2. Vytvořte proces pracovního postupu pro tabulku **Dodavatel** a vyberte šablonu procesu pracovního postupu **Aktualizace dodavatelů typu Osoba v tabulce Kontakty**. Pak vyberte **OK**. Tento workflow zpracovává scénář aktualizace dodavatele pro tabulku **Kontakt**.
3. Vytvořte proces pracovního postupu pro tabulku **Kontakt** a vyberte šablonu **Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé**.
4. Vytvořte proces pracovního postupu pro tabulku **Kontakt** a vyberte šablonu **Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé**.
5. Pracovní postupy můžete konfigurovat buď jako workflowy v reálném čase nebo na pozadí v závislosti na vašich požadavcích. Chcete-li nakonfigurovat workflow jako workflow na pozadí, vyberte možnost **Převést na workflow na pozadí**.
6. Aktivujte pracovní postupy, které jste vytvořili pro tabulky **Kontakt** a **Dodavatel**, abyste mohli začít používat tabulku **Kontakt** k ukládání informací pro dodavatele typu **Osoba**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]