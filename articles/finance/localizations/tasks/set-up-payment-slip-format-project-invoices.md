---
title: Nastavení formátu platebního dokladu pro faktury projektů
description: Společnosti obvykle přiřadí vytištěné platební doklady k fakturám, aby poskytli asistenci odběratelům a určili platební odkaz pro zaúčtování a vyrovnání.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cca7ceb3c862d8a7b2d5a88111b9b3ea46a6c9ea
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988067"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Nastavení formátu platebního dokladu pro faktury projektů

[!include [banner](../../includes/banner.md)]

Společnosti obvykle přiřadí vytištěné platební doklady k fakturám, aby poskytli asistenci odběratelům a určili platební odkaz pro zaúčtování a vyrovnání. Kromě prodejních a volných faktur můžete platební doklad použít i pro faktury za projekt nebo služby, upomínky, oznámení úroků a výpisy z účtu. Chcete-li zpracovat platební doklady, nejprve nastavte identifikační číslo příjemce a formáty přílohy platebního dokladu.

Tato procedura používá ukázkovou společnost DEMF. 

Tato funkce je k dispozici pro právnické osoby, jejichž primární adresa je v Dánsku.


## <a name="set-up-a-creditor-id-number"></a>Nastavte číslo ID příjemce
1. Přejděte do části na Správa organizace > Organizace > Právnické osoby.
2. Rozbalte nebo sbalte oddíl Informace o bankovním účtu.
3. Klikněte na položku Upravit.
4. Zadejte typ a hodnotu do pole ID věřitele FI.
5. Klikněte na položku Uložit.
6. Zavřete stránku.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Nastavení formátu platebního dokladu pro faktury, poznámky, upomínky a výkazy
1. Přejděte do nabídky Pohledávky > Nastavení > Formuláře > Nastavení formuláře.
2. Klikněte na kartu Faktura.
3. Vyberte požadovanou možnost v příloze přidružené platby pole faktury odběratele.
    * Žádné – Netisknout platební doklad. Tuto možnost vyberte, pokud je částka platby v jiné měně než Dánská koruna (DKK).   FIK 751 – Pokud chcete ručně napsat částku platby a datum splatnosti na platební doklad, vytiskněte platební doklad FIK 751.   FIK 752 – Vytiskněte platební doklad FIK 752, pokud máte v úmyslu použít počítačově generovaný platební doklad s předtištěnou částkou platby a datem splatnosti.  
4. Klikněte na položku Uložit.
5. Klikněte na kartu Volná faktura.
6. Vyberte požadovanou možnost v příloze přidružené platby pole volné faktury.
    * Žádné – Netisknout platební doklad. Tuto možnost vyberte, pokud je částka platby v jiné měně než Dánská koruna (DKK).   FIK 751 – Pokud chcete ručně napsat částku platby a datum splatnosti na platební doklad, vytiskněte platební doklad FIK 751.   FIK 752 – Vytiskněte platební doklad FIK 752, pokud máte v úmyslu použít počítačově generovaný platební doklad s předtištěnou částkou platby a datem splatnosti.  
7. Klikněte na položku Uložit.
8. Klikněte na kartu Oznámení úroků.
9. Vyberte požadovanou možnost v příloze přidružené platby pole oznámení úroků.
    * Žádné – Netisknout platební doklad. Tuto možnost vyberte, pokud je částka platby v jiné měně než Dánská koruna (DKK).   FIK 751 – Pokud chcete ručně napsat částku platby a datum splatnosti na platební doklad, vytiskněte platební doklad FIK 751.   FIK 752 – Vytiskněte platební doklad FIK 752, pokud máte v úmyslu použít počítačově generovaný platební doklad s předtištěnou částkou platby a datem splatnosti.  
10. Klikněte na položku Uložit.
11. Klikněte na kartu Upomínka.
12. Vyberte požadovanou možnost v příloze přidružené platby pole upomínky.
    * Žádné – Netisknout platební doklad. Tuto možnost vyberte, pokud je částka platby v jiné měně než Dánská koruna (DKK).   FIK 751 – Pokud chcete ručně napsat částku platby a datum splatnosti na platební doklad, vytiskněte platební doklad FIK 751.   FIK 752 – Vytiskněte platební doklad FIK 752, pokud máte v úmyslu použít počítačově generovaný platební doklad s předtištěnou částkou platby a datem splatnosti.  
13. Klikněte na položku Uložit.
14. Klikněte na kartu Výpis z účtu.
15. Vyberte požadovanou možnost v příloze přidružené platby v poli výpis z účtu.
    * Žádné – Netisknout platební doklad. Tuto možnost vyberte, pokud je částka platby v jiné měně než Dánská koruna (DKK).   FIK 751 – Pokud chcete ručně napsat částku platby a datum splatnosti na platební doklad, vytiskněte platební doklad FIK 751.   FIK 752 – Vytiskněte platební doklad FIK 752, pokud máte v úmyslu použít počítačově generovaný platební doklad s předtištěnou částkou platby a datem splatnosti.  
16. Klikněte na položku Uložit.
17. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]