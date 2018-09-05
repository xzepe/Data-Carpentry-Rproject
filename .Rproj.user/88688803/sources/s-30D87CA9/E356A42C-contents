library("tidyverse")
str(surveys)
#select column
select(surveys, species_id, weight)
#select rows
filter(surveys, year==1995)
#pipes: %>% 


surveys %>% 
  filter(year==1995) %>% 
  select(species_id,weight)

#

exercice <- surveys %>% 
  filter(weight<5) %>% 
  select(species_id, sex, weight)

#creatng a new column
kgs <- surveys %>% 
  mutate(weight_kg=weight/1000)


kg2<- surveys %>% 
  mutate(weight_kg=weight/1000, weight_kg2=weight_kg*2)

head(kg2)

kg2 %>% 
  mutate(weight_kg=weight/1000, weight_kg2=weight_kg*2) %>% 
  head()

kg2 %>% 
  filter(!is.na(weight)) %>% 
mutate(weight_kg=weight/1000, weight_kg2=weight_kg*2) %>% 
  head()

kg %>% 
  filter(!is.na(weight)) %>% 
  mutate(weight_kg=weight/1000, weight_kg2=weight_kg*2) %>% 
  head()

surveys %>% 
  filter(!is.na(weight)) %>% 
  mutate(weight_kg=weight/1000, weight_kg2=weight*2) %>% 
  head()
#group by two columnssurvey
surveys %>% 
  filter(!sex=="") %>% 
  group_by(sex) %>% 
  summarise(mean_weight=mean(weight,na.rm = TRUE))

summarise_two <- surveys %>% 
  filter(!sex=="") %>% 
  filter(!is.na(weight)) %>% 
  group_by(sex,species_id) %>% 
  summarise(mean_weight=mean(weight))


summarise_two <- surveys %>% 
  filter(!sex=="") %>% 
  filter(!is.na(weight)) %>% 
  group_by(sex,species_id) %>% 
  summarise(mean_weight=mean(weight),min_weight=min(weight), max_weight=max(weight))

#Countng

surveys %>% 
  filter(!sex=="") %>% 
  count(sex,species)

#Sorting  ARRAnge

surveys %>% 
  filter(!sex=="") %>% 
  count(sex,species) %>% 
  arrange(species,desc(n))







