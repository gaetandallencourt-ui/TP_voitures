classDiagram
  class CRoue {
    -double m_diametre
    -string m_garniture
    -string m_marque
    -double m_pression
    +CRoue()
    +CRoue(diametre, garniture, marque, pression)
    +affiche() void
    +getDiametre() double
    +getGarniture() string
    +getMarque() string
    +getPression() double
    +setDiametre(diametre) void
    +setGarniture(garniture) void
    +setMarque(marque) void
    +setPression(pression) void
  }

  class CVoiture {
    -string m_marque
    -string m_modele
    -string m_carburant
    -int m_puissance
    -int m_vitesse
    -double m_posX
    -double m_posY
    -double m_kilometrageTotal
    -CRoue m_roues[4]
    +CVoiture(marque, modele, puissance, carburant, diametreRoue, garnitureRoue, marqueRoue, pressionRoue)
    +demarrer() void
    +arreter() void
    +accelerer(vitesse) void
    +ralentir(vitesse) void
    +affiche() void
    +deplacer(deltaX, deltaY) void
    +afficherPosition() void
    +afficheRoues() void
    +getPosX() double
    +getPosY() double
    +getKilometrageTotal() double
    +setPosX(posX) void
    +setPosY(posY) void
  }

  CVoiture "1" *-- "4" CRoue : possède