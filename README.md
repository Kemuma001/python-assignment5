1.Design Your Own Class! 🏗️


              class Project:
                def __init__(self, name, description, deadline, team_members=None):
                            """
                     Initialize a new project with a name, description, deadline, and team members.
                            """
                     self.name = name
                     self.description = description
                     self.deadline = deadline
                     self.team_members = team_members if team_members else [] 
                     self.status = "Not Started"  # Default status

              def add_member(self, member_name):
                    """
                Add a team member to the project.
                    """
                    self.team_members.append(member_name)
                    print(f"{member_name} has been added to the project!")

             def update_status(self, new_status):
                   """
                Update the project status.
                   """
                    self.status = new_status
                    print(f"Project status updated to: {self.status}")

               def show_details(self):
                  """
              Display project details.
                  """
                  print(f"Project Name: {self.name}")
                  print(f"Description: {self.description}")
                  print(f"Deadline: {self.deadline}")
                  print(f"Team Members: {', '.join(self.team_members) if self.team_members else 'None'}")
                  print(f"Status: {self.status}")




2.Create a class representing anything you like (a Smartphone, Book, or even a Superhero!).



          class Superhero:
             def __init__(self, name, alias, superpower, strength_level=50):
                  """
                Initialize the superhero with their real name, alias, superpower, and strength level.
                  """
                   self.name = name
                   self.alias = alias
                   self.superpower = superpower
                   self.strength_level = strength_level
                   self.missions_completed = 0
 
            def train(self, hours):
               """
              Train to increase strength level.
               """
                   self.strength_level += hours * 5
                   print(f"{self.alias} has trained for {hours} hours! Strength increased to {self.strength_level}.")

            def complete_mission(self, mission_name):
                 """
                 Complete a mission and gain experience.
                  """
                    self.missions_completed += 1
                    self.strength_level += 10
                    print(f"{self.alias} completed the mission: {mission_name}.")
                    print(f"Strength is now {self.strength_level}. Missions completed: {self.missions_completed}")

             def show_profile(self):
                """
                Display the superhero's profile.
                 """
                  print(f"Superhero Profile:")
                  print(f"Real Name: {self.name}")
                  print(f"Alias: {self.alias}")
                  print(f"Superpower: {self.superpower}")
                  print(f"Strength Level: {self.strength_level}")
                  print(f"Missions Completed: {self.missions_completed}")




3.Add attributes and methods to bring the class to life!




        class Superhero:
               def __init__(self, name, alias, superpower, strength_level=50, weakness="None"):
                """
               Initialize the superhero with key attributes.
                """
                  self.name = name
                  self.alias = alias
                  self.superpower = superpower
                  self.strength_level = strength_level
                  self.weakness = weakness
                  self.missions_completed = 0
                 self.allies = []
                 self.arch_nemesis = None
                 self.battle_log = []

           def train(self, hours):
               """
              Train to increase strength level.
              """
                self.strength_level += hours * 5
                print(f"{self.alias} trained for {hours} hours. Strength is now {self.strength_level}.")

          def complete_mission(self, mission_name):
                 """
             Complete a mission and gain experience.
                 """
               self.missions_completed += 1
               self.strength_level += 10
               print(f"{self.alias} completed the mission: {mission_name}.")
               print(f"Strength is now {self.strength_level}. Missions completed: {self.missions_completed}.")

          def add_ally(self, ally_name):
              """
             Add an ally to the superhero's team.
              """
               self.allies.append(ally_name)
               print(f"{ally_name} has joined {self.alias}'s team!")

          def set_arch_nemesis(self, nemesis_name):
              """
            Set an arch-nemesis for the superhero.
              """
               self.arch_nemesis = nemesis_name
               print(f"{self.alias}'s arch-nemesis is now {self.arch_nemesis}.")

         def fight_battle(self, opponent_name, difficulty_level):
              """
             Simulate a battle against an opponent.
              """
               print(f"{self.alias} is battling {opponent_name}!")
            if difficulty_level > self.strength_level:
               self.strength_level -= 10
               result = f"Lost to {opponent_name}."
              print(f"{self.alias} lost the battle. Strength reduced to {self.strength_level}.")
           else:
               self.strength_level += 15
              result = f"Defeated {opponent_name}!"
               print(f"{self.alias} won the battle! Strength increased to {self.strength_level}.")
        
          self.battle_log.append({"opponent": opponent_name, "result": result})

        def show_profile(self):
                 """
             Display the superhero's profile.
                  """
               print("\n--- Superhero Profile ---")
               print(f"Real Name: {self.name}")
               print(f"Alias: {self.alias}")
               print(f"Superpower: {self.superpower}")
               print(f"Strength Level: {self.strength_level}")
               print(f"Weakness: {self.weakness}")
               print(f"Missions Completed: {self.missions_completed}")
               print(f"Allies: {', '.join(self.allies) if self.allies else 'None'}")
               print(f"Arch-Nemesis: {self.arch_nemesis if self.arch_nemesis else 'None'}")

        def show_battle_log(self):
               """
              Display all battles fought by the superhero.
                """
                print("\n--- Battle Log ---")
           if not self.battle_log:
                print(f"{self.alias} hasn't fought any battles yet.")
          else:
                for battle in self.battle_log:
                print(f"Opponent: {battle['opponent']} | Result: {battle['result']}")




4.Use constructors to initialize each object with unique values.



      class Superhero:
           def __init__(self, name, alias, superpower, strength_level, weakness):
        """
        Initialize the superhero with unique values for each object.
        """
             self.name = name
             self.alias = alias
             self.superpower = superpower
             self.strength_level = strength_level
             self.weakness = weakness
             self.missions_completed = 0
             self.allies = []
             self.arch_nemesis = None
             self.battle_log = []

        def train(self, hours):
        """
      Train to increase strength level.
        """
             self.strength_level += hours * 5
             print(f"{self.alias} trained for {hours} hours. Strength is now {self.strength_level}.")

         def complete_mission(self, mission_name):
        """
     Complete a mission and gain experience.
        """
             self.missions_completed += 1
            self.strength_level += 10
            print(f"{self.alias} completed the mission: {mission_name}.")
            print(f"Strength is now {self.strength_level}. Missions completed: {self.missions_completed}.")

         def add_ally(self, ally_name):
        """
      Add an ally to the superhero's team.
        """
           self.allies.append(ally_name)
           print(f"{ally_name} has joined {self.alias}'s team!")


          def set_arch_nemesis(self, nemesis_name):
        """
       Set an arch-nemesis for the superhero.
        """
           self.arch_nemesis = nemesis_name
           print(f"{self.alias}'s arch-nemesis is now {self.arch_nemesis}.")

      def fight_battle(self, opponent_name, difficulty_level):
        """
       Simulate a battle against an opponent.
        """
              print(f"{self.alias} is battling {opponent_name}!")
          if difficulty_level > self.strength_level:
              self.strength_level -= 10
              result = f"Lost to {opponent_name}."
              print(f"{self.alias} lost the battle. Strength reduced to {self.strength_level}.")
          else:
               self.strength_level += 15
               result = f"Defeated {opponent_name}!"
               print(f"{self.alias} won the battle! Strength increased to {self.strength_level}.")
        
           self.battle_log.append({"opponent": opponent_name, "result": result})

        def show_profile(self):
        """
       Display the superhero's profile.
        """
              print("\n--- Superhero Profile ---")
              print(f"Real Name: {self.name}")
              print(f"Alias: {self.alias}")
              print(f"Superpower: {self.superpower}")
              print(f"Strength Level: {self.strength_level}")
              print(f"Weakness: {self.weakness}")
              print(f"Missions Completed: {self.missions_completed}")
              print(f"Allies: {', '.join(self.allies) if self.allies else 'None'}")
              print(f"Arch-Nemesis: {self.arch_nemesis if self.arch_nemesis else 'None'}")

          def show_battle_log(self):
            """
       Display all battles fought by the superhero.
        """
              print("\n--- Battle Log ---")
           if not self.battle_log:
              print(f"{self.alias} hasn't fought any battles yet.")
          else:
               for battle in self.battle_log:
                print(f"Opponent: {battle['opponent']} | Result: {battle['result']}")




5.Add an inheritance layer to explore polymorphism or encapsulation.



          class Hero:
      """
     Base class for all types of heroes.
      """
     def __init__(self, name, alias, strength_level, weakness):
           self.name = name
          self.alias = alias
          self.strength_level = strength_level
          self.weakness = weakness
          self.missions_completed = 0

     def show_profile(self):
          """
          Display the hero's profile.
           """
           print(f"\n--- {self.__class__.__name__} Profile ---")
           print(f"Real Name: {self.name}")
           print(f"Alias: {self.alias}")
           print(f"Strength Level: {self.strength_level}")
           print(f"Weakness: {self.weakness}")
           print(f"Missions Completed: {self.missions_completed}")

      def train(self, hours):
           """
          Train to increase strength level.
          """
            self.strength_level += hours * 5
            print(f"{self.alias} trained for {hours} hours. Strength increased to {self.strength_level}.")

     def complete_mission(self, mission_name):
           """
         Complete a mission to gain experience.
          """
           self.missions_completed += 1
           self.strength_level += 10
           print(f"{self.alias} completed the mission: {mission_name}. Strength increased to {self.strength_level}.")

     class Superhero(Hero):
          """
       Derived class for superheroes.
           """
     def __init__(self, name, alias, superpower, strength_level, weakness):
           super().__init__(name, alias, strength_level, weakness)
           self.superpower = superpower

     def use_superpower(self):
            """
           Use the superhero's superpower.
             """
            print(f"{self.alias} is using their superpower: {self.superpower}!")

     def show_profile(self):
            """
         Display the superhero's profile, including superpower.
           """
             super().show_profile()
             print(f"Superpower: {self.superpower}")


      class Villain(Hero):
          """
         Derived class for villains.
           """
       def __init__(self, name, alias, evil_plan, strength_level, weakness):
           super().__init__(name, alias, strength_level, weakness)
           self.evil_plan = evil_plan

       def execute_evil_plan(self):
            """
           Execute the villain's evil plan.
            """
               print(f"{self.alias} is executing their evil plan: {self.evil_plan}!")

       def show_profile(self):
               """
           Display the villain's profile, including evil plan.
             """
               super().show_profile()
               print(f"Evil Plan: {self.evil_plan}")
