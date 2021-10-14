---
title: Vytvoření šablon pracovní doby
description: Šablony pracovní doby definují pracovní dobu v týdnu a slouží ke generování pracovní doby pro časový úsek.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130a21d08e4e720f8bf803a5d4b03d315cefc26f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580665"
---
# <a name="create-working-time-templates"></a>Vytvoření šablon pracovní doby

[!include [banner](../../includes/banner.md)]

Šablony pracovní doby definují pracovní dobu v týdnu a slouží ke generování pracovní doby pro časový úsek. Tento postup popisuje, jak definovat šablony pracovní doby pomocí vlastností plánování pracovní doby pro zařazení časových intervalů práce. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.

1. Přejděte na **Pracovní prostory > Správa životního cyklu prostředků**.
1. Vyberte **Šablon pracovní doby**.

## <a name="create-working-time-template"></a>Vytvoření šablony pracovní doby

1. Zvolte **Nové**.
1. Zadejte hodnotu do pole **Šablona pracovní doby**.
1. Zadejte hodnotu do pole **Název**.
1. Rozbalte sekci **Pondělí**.
1. Vyberte **přidat**.
1. Do pole **Od** zadejte čas.
    * Určete čas při zahájení práce ráno.  
1. Do pole **Do** zadejte čas.
    * Zadejte čas, kdy zaměstnanci mají přestávku na oběd.  
1. Vyberte **přidat**.
1. Do pole **Od** zadejte čas.
    * Zadejte čas, kdy práci obnoví po obědě.  
1. Do pole **Do** zadejte čas.
    * Určete konec pracovního dne.  

## <a name="replicate-working-times-to-all-week-days"></a>Replikace pracovní doby pro všechny dny v týdnu

1. Vyberte **Kopírovat den**.
    * Zkopírujte definice pracovní doby od pondělí do úterý.  
1. Vyberte **OK**.
1. Vyberte **Kopírovat den**.
    * Zkopírujte definice pracovní doby od pondělí do středa.  
1. Vyberte volbu v poli **Do pracovního dne**.
1. Vyberte **OK**.
1. Vyberte **Kopírovat den**.
    * Zkopírujte definice pracovní doby od pondělí do čtvrtka.  
1. Vyberte volbu v poli **Do pracovního dne**.
1. Vyberte **OK**.
1. Vyberte **Kopírovat den**.
    * Zkopírujte definice pracovní doby od pondělí do pátku.  
1. Vyberte volbu v poli **Do pracovního dne**.
1. Vyberte **OK**.

## <a name="define-time-slots-for-special-operations"></a>Definování časových úseků pro zvláštní operace

1. Rozbalte sekci **Pátek**.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
1. V poli **Vlastnosti** zadejte nebo vyberte hodnotu.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
1. V poli **Vlastnosti** zadejte nebo vyberte hodnotu.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Označení víkendových dnů jako uzavřených pro výdej

1. Rozbalte sekci **Sobota**.
1. Vyberte možnost *Ano* v poli **Uzavřeno pro výdej**.
1. Rozbalte sekci **Neděle**.
1. Vyberte možnost *Ano* v poli **Uzavřeno pro výdej**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]