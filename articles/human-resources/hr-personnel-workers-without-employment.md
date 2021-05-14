---
title: Pracovníci bez zaměstnání
description: Pracovníci bez budoucího, aktivního nebo historického zaměstnání ve vaší organizaci se objeví ve formuláři Pracovníci bez zaměstnání.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924564"
---
# <a name="workers-without-employment"></a>Pracovníci bez zaměstnání

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Pracovníci bez budoucího, aktivního nebo historického zaměstnání ve vaší organizaci se objeví ve formuláři **Pracovníci bez zaměstnání**. Pracovníci s tímto stavem se mohou objevit, když importujete pracovníky bez záznamu o zaměstnání nebo když odstraníte zaměstnání pracovníka prostřednictvím **Pracovníci > Historie zaměstnání**.

Ve výchozím nastavení je formulář **Pracovníci bez zaměstnání** k dispozici pro následující role:

- Asistent lidských zdrojů
- Manažer lidských zdrojů
- Náborový pracovník
- Manažer kompenzací a zaměstnaneckých výhod
- Správce mezd
- Manažer mezd
- Manažer školení

V seznamu **Pracovníci bez zaměstnání** můžete odstranit uvedené osoby. Ve výchozím nastavení je toto oprávnění uděleno roli asistenta lidských zdrojů. Toto oprávnění můžete udělit dalším rolím pomocí následujících kroků:

1. Vyberte **Správa systému** a poté vyberte kartu **Konfigurace zabezpečení**.

2. Na kartě **Oprávnění** vyfiltrujte seznam **Oprávnění**, aby bylo možné **spravovat pracovníky**.

   [![Filtrovat seznam oprávnění](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. Ve sloupci **Reference** vyberte **zobrazit položky nabídky**.

4. V **Zobrazit položky nabídky** vyberte **HcmWorkersWithoutEmployment**.

   [![Zvolit formulář](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. Nastavte oprávnění **Odstranit** na **Udělit**.

6. Vyberte kartu **nepublikované objekty**.

7. Zvolte **Publikovat vše**.

   [![Publikovat změny](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]