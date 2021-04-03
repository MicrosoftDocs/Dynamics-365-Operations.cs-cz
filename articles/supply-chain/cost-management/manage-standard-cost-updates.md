---
title: Správa aktualizací standardních nákladů
description: Aktualizace dat standardních nákladů lze spravovat pomocí dvou různých metod – metody s jednou verzí nebo se dvěma verzemi.
author: AndersGirke
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: fc4ae40e9740ce76e79b76c2bff2c690568abff2
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500591"
---
# <a name="manage-standard-cost-updates"></a>Správa aktualizací standardních nákladů

[!include [banner](../includes/banner.md)]

Aktualizace dat standardních nákladů lze spravovat pomocí dvou různých metod – metody s jednou verzí nebo se dvěma verzemi.

Metoda s jednou verzí používá jednu nákladovou verzi obsahující všechny záznamy o nákladech. Tyto záznamy zahrnují původní náklady a všechny aktualizace nákladů.

Metoda se dvěma verzemi využívá jednu verzi, která obsahuje záznamy o původních nákladech, a druhou verzi, která obsahuje záznamy o všech aktualizacích nákladů. Hlavní výhodou metody se dvěma verzemi je jasné zobrazení a možnost sledování aktualizací nákladů v samostatné verzi nákladů, bez ovlivnění původní verze nákladů. Metodu se dvěma verzemi lze použít k identifikaci více přírůstkových aktualizací, kdy každé přírůstkové aktualizaci bude odpovídat samostatná verze nákladů obsahující přírůstkové záznamy nákladů.

## <a name="example"></a>Příklad

Následující příklad znázorňuje použití přístupu s jednou verzí a dvěma verzemi pro aktualizace standardních nákladů ve výrobním prostředí. Například aktualizace odpovídající novým položkám nebo opravám chyb. Předpokládejme, že jedna nákladová verze reprezentuje standardní náklady pro aktuální rok. Identifikátor pro tuto verzi je 2020-STD. Verze 2020-STD obsahuje aktuální aktivní náklady pro všechny položky. Dále obsahuje aktuální aktivní náklady pro všechny položky a všechny nákladové kategorie související s postupy a vzorce výpočtu režie, které byly známy na počátku roku 2020. 2020-STD je původní verze ocenění.

- **Metoda aktualizace údajů nákladů s použitím jedné verze** − Metoda s jednou verzí znamená, že původní nákladová verze 2020-STD bude obsahovat všechny záznamy nákladů. Aktualizace nákladů jsou zaznamenány do 2020-STD a jsou nastavena na stav Nevyřízené. Náklady se stavem nevyřízeno mohou být například ručně zadány pro nově zakoupené položky nebo mohou být vypočteny pro určitou vyrobenou položku s cílem zohlednit opravy. Při použití způsobu jedné verze výpočty kusovníku nevyžadují vytvoření záložního zdroje dat, protože v nákladové verzi jsou obsaženy všechny aktivní náklady. Po aktivaci nevyřízených nákladů bude původní nákladová verze 2020-STD znovu obsahovat všechny aktuální aktivní náklady.
- **Metoda aktualizace údajů nákladů s použitím dvou verzí** − Metoda se dvěma verzemi vyžaduje další nákladovou verzi, která bude obsahovat pouze aktualizace nákladů. Identifikátor pro tuto verzi je 2020-STD-CHANGES. Aktualizace nákladů jsou zaznamenány do 2020-STD-CHANGES a jsou nastaveny na stav Nevyřízené. Výpočty kusovníku nevyřízených nákladů pro vyrobené položky u metody dvou verzí vyžadují záložní datový zdroj. Důvodem je skutečnost, že dodatečná nákladová verze 2020-STD-CHANGES obsahuje pouze podmnožinu dat nákladů. Zálohu lze vyjádřit jako aktivní náklady nebo jako nákladovou verzi 2020-STD, protože obě tyto položky identifikují zdroj dat nákladů v případech, kdy tento zdroj neexistuje ve verzi 2020-STD-CHANGES. Po aktivaci nákladů se stavem nevyřízeno bude dodatečná nákladová verze 2020-STD-CHANGES obsahovat aktuální aktivní náklady odrážející aktualizace, přičemž původní nákladová verze 2020-STD nebude ovlivněna. Použití metody se dvěma verzemi znamená, že pomocí zásad blokování pro původní nákladovou verzi je zabráněno aktualizacím. Identické zásady blokování by měly být nastaveny pro dodatečnou nákladovou verzi, s výjimkou zadaného počátečního data a selektivního použití zásad blokování pro umožnění aktualizací. Určené počáteční datum musí být s každou dávkou změn aktualizováno, aby odpovídalo naplánovanému datu aktivace.

V tomto příkladu byla použita dodatečná nákladová verze pro správu aktualizací v průběhu roku 2020. Lze použít více dodatečných nákladových verzí (například samostatnou verzi pro každou dávku aktualizací). Při použití více dalších nákladů musí být záloha vyjádřena jako aktivní náklady, protože aktivní náklady jsou rozděleny na více nákladových verzích.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Finanční dimenze pro standardní přecenění nákladů

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Aktivace nové standardní ceny obvykle přecení aktuální hodnotu zásob standardními transakcemi přecenění nákladů. Finanční dimenze položky se pak zaúčtují na transakcích. hcete-li však určit, zda a jak jsou finanční dimenze zaúčtovány, použijte [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) k zapnutí funkce nazvané *Možnosti výchozí finanční dimenze pro přecenění standardních nákladů na zásoby*. Po povolení této funkce přejděte na **Správa nákladů> Nastavení zásad účtování zásob> Parametry** a nastavte nový rozevírací seznam **Původ finanční dimenze** na jednu z následujících hodnot:

- **Žádný** - žádné finanční dimenze nebyly zaúčtovány pro transakce zaměřené na přecenění cizí měny. Pokud vaše účetní struktura zahrnuje požadovanou finanční dimenzi ve vaší účetní struktuře, proces přecenění stále probíhá, ale vytvoří účetní položky, které nemají žádné finanční dimenze. V takovém případě uživatelé nejprve obdrží varovnou zprávu, aby mohli v případě potřeby přecenění zrušit.
- **Tabulka** – Finanční dimenze položky se pak zaúčtují na transakcích přecenění. Toto je výchozí nastavení a je v souladu s původním chováním systému bez zapnutí funkce *Možnosti výchozí finanční dimenze pro přecenění standardních nákladů na zásoby*.
- **Zaúčtování** – finanční dimenze transakce, která je právě přehodnocena, je zaúčtována v transakcích přecenění. Ve výchozím nastavení se finanční dimenze z účtu zásob původní transakce použijí jak pro účet inventáře, tak pro účet přecenění.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]