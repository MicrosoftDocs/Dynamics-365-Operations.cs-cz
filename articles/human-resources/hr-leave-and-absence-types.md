---
title: Konfigurace typů pracovního volna a absence
description: Nastavte typy volna, které mohou zaměstnanci provést v aplikaci Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008394"
---
# <a name="configure-leave-and-absence-types"></a>Konfigurace typů pracovního volna a absence

Typy pracovního volna v Dynamics 365 Human Resources definují různé typy absence, které může zaměstnanec ohlásit. Typy pracovního volna můžete přizpůsobit podle potřeb dané organizace. Příklady popisů typů pracovního volna:

- Placený čas volna (PTO)
- Neplacené volno
- Placená dovolená
- Pracovní neschopnost
- Zdravotní dovolená
- Volno z rodinných důvodů
- Krátkodobá invalidita
- Volno z důvodu zármutku

## <a name="add-a-leave-type"></a>Přidání typu pracovního volna

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V části **Nastavení** vyberte **Typ pracovního volna a absence**.

3. Zvolte **Nové**.

4. Zadejte název typu pracovního volna v části **Typ**, vyberte workflow v okně **ID workflowu** a do pole **Popis** napište popis.

5. V části **Obecné** vyberte **Žádný**, **Naplánované** nebo **Neplánované** v rozevíracím seznamu **Kategorie**.

6. Vyberte kód výdělku z rozevíracího seznamu **kód výdělku**.

7. V části **Požadován kód důvodu** vyberte, zda chcete požadovat kód důvodu. Chcete-li požadovat kódy důvodu, budete je pravděpodobně muset přidat. V části **Kódy důvodu** vyberte možnost **Přidat**, vyberte kód důvodu a poté zaškrtněte políčko **Povoleno** vedle něho.

8. V části **Omezit přístup k vybraným rolím** vyberte, zda chcete omezit přístup. Poté vyberte role zabezpečení v části **role zabezpečení pro tento typ pracovního volna**. Role zabezpečení jsou definovány ve workflowu vybraném pod položkou **ID workflowu** dříve v tomto postupu.

9. Zvolte **Uložit**.

## <a name="configure-preview-features"></a>Konfigurace funkcí náhledu

Pokud jste povolili funkce náhledu pro pracovní volno a absenci, musíte pro ně také nakonfigurovat nastavení.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. Nastavte možnosti zaokrouhlení pro typ pracovního volna. Možnosti zahrnují **Žádný** **Nahoru**, **Dolů** a **Nejbližší**. Můžete také nastavit přesnost zaokrouhlení pro typ pracovního volna.

2. Nastavte **Oprava volna** pro typ pracovního volna. Pokud vyberete tuto možnost, aplikace Human Resources použije počet svátků, které spadají do pracovního dne k určení, jakým způsobem má být rozlišen volný čas u tohoto typu pracovního volna. Pokud například 1. svátek vánoční připadá na pondělí, odečte aplikace Human Resources při zpracování časového rozlišení od typu pracovního volna jeden den.

   Svátky nastavujete v kalendáři pracovní doby. Další informace naleznete v tématu [Vytvoření kalendáře pracovní doby](hr-leave-and-absence-working-time-calendar.md)

## <a name="see-also"></a>Viz také

- [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)
- [Vytvoření plánu pracovního volna a absence](hr-leave-and-absence-plans.md)
- [Vytvoření kalendáře pracovní doby](hr-leave-and-absence-working-time-calendar.md)