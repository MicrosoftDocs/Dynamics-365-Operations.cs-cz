---
title: Návrh konfigurací pro generování sestav ve formátech Office s integrovanými obrázky
description: Tento článek popisuje proces navrhování konfigurací, které generují elektronické dokumenty ve formátech Excel a Word, které obsahují vestavěné obrázky.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 255b9a4e5276a9a80a4fbc15076f78a25c918e80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886636"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Návrh konfigurací pro generování sestav ve formátech Office s integrovanými obrázky

[!include [banner](../../includes/banner.md)]

K provedení kroků v tomto postupu musíte nejprve dokončit postup "Elektronické výkaznictví - Vytvoření poskytovatele konfigurace a jeho označení jako aktivního." Tento postup vysvětluje proces navrhování konfigurací elektronického výkaznictví pro generování dokumentů v aplikacích Microsoft Excel nebo Word obsahujících vložené obrázky. V tomto postupu vytvoříte požadované konfigurace elektronického výkaznictví pro vzorovou společnost Litware, Inc. Tyto kroky lze dokončit pomocí sady dat USMF. Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Před přihlášením je také nutné stáhnout a uložit následující soubory: 

| popis                                          | Název souboru                   |
|------------------------------------------------------|-----------------------------|
| Konfigurace datového modelu elektronického výkaznictví                          | [Model pro cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| Konfigurace formátu elektronického výkaznictví                              | [format.xml pro tisk šeků](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Obrázek loga společnosti                                   | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Podpisový obrázek                                      | [Signature image.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternativní podpisový obrázek                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Šablona Microsoft Word pro tisk platebních šeků  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a>Kontrola předpokladů  
 1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.  
 2. Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".   
 3. Klikněte na Konfigurace výkaznictví.  
 
## <a name="add-a-new-er-model-configuration"></a>Přidání nové konfigurace ER modelu  
 1. Namísto vytváření nových modelů můžete načíst dříve uložený konfigurační soubor modelu ER (Model pro cheques.xml). Tento soubor obsahuje ukázkový datový model pro platby šekem a mapování datového modelu na datové komponenty aplikace Dynamics 365 for Operations.   
 2. Na pevné záložce Verze klepněte na tlačítko Exchange.   
 3. Klikněte na Načíst ze souboru XML.  
 4. Klepněte na tlačítko Procházet a vyberte Model pro cheques.xml.   
 5. Klikněte na tlačítko OK.  
 6. Načtený model bude použit jako datový zdroj informací pro generování dokumentů, které obsahují obrázky v aplikaci Excel a Word.  

## <a name="add-a-new-er-format-configuration"></a>Přidání nové konfigurace formátu ER  
 1. Namísto vytváření nových formátů můžete načíst dříve uložený konfigurační soubor formátu ER (Tisk šeků format.xml). Tento soubor obsahuje ukázkové rozložení formátu tisku šeků pomocí předtištěného formuláře a mapování tohoto formátu na model pro 'datový model šeků'.   
 2. Klikněte na Směna.  
 3. Klikněte na Načíst ze souboru XML.  
 4. Klepněte na tlačítko Procházet a vyberte soubor Cheques printing format.xml.   
 5. Klikněte na tlačítko OK.  
 6. Ve stromové struktuře rozbalte Model pro šeky.  
 7. Ve stromovém zobrazení vyberte Model for cheques\Cheques printing format.  
 8. Načtený formát bude použit jako datový zdroj informací pro generování dokumentů, které obsahují obrázky v aplikaci Excel a Word.   

## <a name="configure-er-user-parameters"></a>Konfigurace parametrů uživatele ER  
 1. V podokně akcí klikněte na možnost Konfigurace.  
 2. Klikněte na Parametry uživatelů.  
 3. Vyberte možnost Ano v poli Nastavení běhu.  
  Zapněte příznak 'Spusťte koncept' tak, aby se spustila pracovní verze ve vybraném formátu namísto dokončené.  
 4. Klikněte na tlačítko OK.  

## <a name="configure-cash--bank-management-parameters"></a>Konfigurovat parametry správy Pokladny a banky  
 1. Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.  
 2. Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'USMF OPER.  
 3. V podokně akcí klikněte na možnost Nastavit.  
 4. Klepněte na možnost Kontrola.  
 5. Rozbalte sekci Nastavení.  
 6. Klikněte na položku Upravit.  
 7. Vyberte Ano v poli Firemní logo.  
 8. Klikněte na Firemní logo.  
 9. Klikněte na tlačítko Změnit.  
 10. Klepněte na tlačítko Procházet a vyberte dříve stažený soubor, Company logo.png.   
 11. Klikněte na položku Uložit.  
 12. Zavřete stránku.  
 13. Rozbalte sekci Podpis.  
 14. Vyberte možnost Ano v poli Tisk prvního podpisu.  
 15. Klikněte na tlačítko Změnit.  
 16. Klepněte na tlačítko Procházet a vyberte dříve stažený soubor, Signature image.png.   
 17. Rozbalte sekci Kopie.  
 18. Vyberte volbu v poli Vodoznak.  
 19. Vyberte možnost Ano v poli Obecný formát exportu.  
 20. Vyberte konfiguraci 'Formulář pro tisk šeků'.  
 21. Nyní bude vybraný formát ER použit pro tisk šeků.  
 22. Klikněte na možnost Připojit.  
 23. Klikněte na položku Nová.  
 24. Klepněte na volby Soubor.  
 25. Klepněte na tlačítko Procházet a vyberte dříve stažený soubor, Signature image 2.png.   
 26. Zavřete stránku.  
 27. Zavřete stránku.  
 28. Zavřete stránku.  
 29. Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.  
 30. Vyberte možnost Ano v poli Povolit vytváření verifikačních transakcí v neaktivních bankovních účtech:.  
 31. Klikněte na položku Uložit.  
 32. Zavřete stránku.  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
